<template>
       <h1>Projects</h1>
<div v-for="projects in Projects" :key="projects.id" class="projects"></div>
 <router-link :to="{name:'ProjectDetails', params: { id:projects.id}}"> 
   <h2>{{ projects.title }}</h2>
 </router-link>
 


  <h1>this is a project</h1>
  <h3>the projects id is {{ id }}</h3>
</template>

<script>
export default {
props:['id'],
data() {
    return {
        projects:null
    }
},

mounted() {
    fetch('http://localhost:3000/projects/1')
     .then((res)=> res.json())
      .then(data=>this.projects=data)
       .catch(err => console.log(err.message))
},

}
</script>

<style>

</style>