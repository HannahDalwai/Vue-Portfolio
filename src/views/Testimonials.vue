<template>
  <Navbar/>

</template>

<script>

import Navbar from '../components/Navbar.vue'

export default {
    components: {Navbar},

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

<style>

</style>