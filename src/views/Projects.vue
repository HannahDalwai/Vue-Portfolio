<template>
<Navbar/>
  <h1>Projects</h1>
  <div v-if="projects.length">
    <div v-for="project in projects" :key="project.id" class="projects">
        <router-link :to="{name:'ProjectDetails', params: { id:project.id}}"> 
          <h2>{{ project.title }}</h2>
        </router-link>
    </div>
  </div>



          <button @click="redirect">Redirect</button>
          <button @click="back"> Go back</button>
          <button @click="forward">Go Forward</button>
</template>

<script>

import Navbar from '../components/Navbar.vue'

export default {

components: {Navbar},

data() {
    return {

        projects:[]
    }
},

mounted() {
    fetch('http://localhost:3000/projects')
     .then((res)=> res.json())
      .then(data => this.projects=data)
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