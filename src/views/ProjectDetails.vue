<template>
<Navbar/>

       <h1>Projects</h1> 
       <div v-if="projects">
        <h3>this is a project</h3>
         <p>the projects id is {{ $route.params.id }}</p>
      </div>
      <div v-else> loading project details</div>
            
</template>

<script>
  import Navbar from '../components/Navbar.vue'


export default {
    components: {Navbar},

      props:['id'],
      data() {
          return {
              projects:null
          }
      },

mounted() {
    fetch('http://localhost:3000/projects/'+ this.id)
     .then((res)=> res.json())
      .then(data=>this.projects=data)
       .catch(err => console.log(err.message))
},

}
</script>

<style>

</style>