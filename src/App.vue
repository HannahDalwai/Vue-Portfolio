<template>
      
    <Navbar/>
    <div class="container"> 
      <button @click="redirect">Redirect</button>
      <button @click="back"> Go back</button>
      <button @click="forward">Go Forward</button> 
     </div>
     
  <router-view/>
</template>

<script>

 import Navbar from '../src/components/Navbar.vue'

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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.container{
  margin-left: 50px;
  
}


</style>
