<template>
    <Navbar/>
    <router-view/>
 <button @click="redirect">Redirect</button>
      <button @click="back"> Go back</button>
      <button @click="forward">Go Forward</button>
</template>

<script>

 import Navbar from '../src/components/Navbar.vue'

export default {
    components: {Navbar},
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


</style>
