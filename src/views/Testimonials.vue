<template>
 <h3>testimonials</h3>

</template>

<script>



export default {
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

<style>

</style>