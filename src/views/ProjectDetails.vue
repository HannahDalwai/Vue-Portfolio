<template>
       <h1>Projects</h1> 
        <h3>this is a project</h3>
         <p>the projects id is {{ $route.params.id }}</p>
        
            
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
    fetch('http://localhost:3000/projects/'+ this.id)
     .then((res)=> res.json())
      .then(data=>this.projects=data)
       .catch(err => console.log(err.message))
},

}
</script>

<style>

</style>