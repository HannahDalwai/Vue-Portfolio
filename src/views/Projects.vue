<template>
            <button @click="redirect">Redirect</button>
            <button @click="back"> Go back</button>
            <button @click="forward">Go Forward</button>
</template>

<script>
export default {
data() {
    return {
        projects:[]
    }
},

mounted() {
    fetch('http://localhost:3000/projects')
     .then((res)=> res.json())
      .then(data=>this.projects=data)
       .catch(err => console.log(err.message))
},

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