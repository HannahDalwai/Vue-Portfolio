<template>


 <h1>Homepage</h1>
   <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam culpa enim nulla? Reprehenderit eligendi magni fugit porro, beatae, asperiores, similique dolore sunt eum placeat illo delectus voluptates iure doloribus rerum?</p>
     
</template>

<script>


export default {
  name: 'Home',
  components: {},
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
