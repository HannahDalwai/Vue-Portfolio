<template>
  
</template>

<script>
export default {
data() {
    return {
        projects:[]
    }
},
1

mounted() {
    fetch('http://localhost:3000/projects')
     .then((res)=> res.json())
      .then(data=>this.projects=data)
      .catch(err => console.log(err.message))
}
}
</script>

<style>

</style>