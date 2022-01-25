<template>
  <button @click="redirect">Redirect</button>
<button @click="back"> Go back</button>
<button @click="forward">Go Forward</button>
</template>

<script>
export default {
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