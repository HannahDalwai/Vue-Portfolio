<template>

    <router-view/>
</template>

<script>
export default {
methods: {
  openNav(){
       document.querySelector("nav").classList.toggle("active");
  }
},
}
</script>

<style>

</style>