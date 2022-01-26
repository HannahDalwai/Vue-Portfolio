<template>
      
    <Navbar/>
    <!-- <div class="container"> 
      <button @click="back"><i class='bx bx-left-arrow-alt bx-fade-left-hover' ></i></button>
      <button @click="redirect"><i class='bx bxs-home' ></i></button>
      <button @click="forward"><i class='bx bx-right-arrow-alt bx-fade-right-hover'></i></button> 
     </div> -->
    <main>
      <router-view/>
    </main>
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
