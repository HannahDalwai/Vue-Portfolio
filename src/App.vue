<template>
    <Navbar/>
    <main>
      <router-view/>
    </main>
</template>

<script>

import Navbar from '../src/components/Navbar.vue'

export default {
    components: {Navbar},
     methods: {},
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
main {
  margin-left: 280px;
  transition: all 0.3s linear;
  display: flex;
 
}


</style>
