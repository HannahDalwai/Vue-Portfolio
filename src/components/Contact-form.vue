<template>
  <form >
      <label >Email</label>
      <input type="email" required v-model="email">
      <label for="Name">Name</label>
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
form{
    max-width: 420x;
    margin:30px auto;
    background: rgb(187, 184, 184);
    text-align: left;
    padding: 40px;
}
label{
    color: #444;
    display:inline-block;
    margin: 25px 0 15px;
    font-size: 0.6rem;
    letter-spacing: 1px;
    text-transform: uppercase;
    width: 100%;
    font-weight:bold;
}
input{
    display: block;
    box-sizing: border-box;
    padding: 10px 6px ;
    border-bottom: 1px solid #ddd;
    color: #555;

}
</style>