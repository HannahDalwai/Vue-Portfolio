<template>

  <h1>Projects</h1>
  <div v-if="projects.length">
    <div v-for="project in projects" :key="project.id" class="projects">
        <router-link :to="{name:'ProjectDetails', params: { id:project.id}}"> 
          <h2>{{ project.title }}</h2>

        </router-link>
    </div>
  </div>
  <div v-else>
    loading projects
  </div>




        
</template>

<script>


export default {

      components: {},

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
      }
         
}
</script>

<style>

</style>