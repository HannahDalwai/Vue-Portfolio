<template>
  
</template>

<script>
export default {

}
</script>
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
<style>

</style>