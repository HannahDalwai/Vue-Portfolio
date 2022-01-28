<template>
  <form >
      <label >Email</label>
      <input type="email" required v-model="email">
      <label for="Name"></label>
       <input type="text" required v-model="name">
      </form>


      <p>Email: {{ email }}</p>
      <p>Name: {{ name }}</p>
</template>

<script>
export default {
data() {
    return {
        email:'',
        name:'',
    }
},
}
</script>

<style>

</style>