<template>
<Navbar/>
<Header title="Hello World"/>
 <h1>Homepage</h1>
   <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam culpa enim nulla? Reprehenderit eligendi magni fugit porro, beatae, asperiores, similique dolore sunt eum placeat illo delectus voluptates iure doloribus rerum?</p>
      <button @click="redirect">Redirect</button>
      <button @click="back"> Go back</button>
      <button @click="forward">Go Forward</button>
</template>

<script>

import Navbar from '../components/Navbar.vue'
import Header from '../components/Header.vue'

export default {
  name: 'Home',
  components: {Navbar,Header},
  methods: {
    redirect(){
       this.$router.push({name:'Home'})
    },
    back(){
      this.$router.go(-1)
    },
    forward(){
       this.$router.go(1)
    }
  },
}
</script>
