<template>
  <!-- <div id="nav" role="navigation" class="nav nav-pills">
  </div> -->


  	<nav role="navigation" class="nav nav-pills">
		<div id="menuToggle">
		  <input type="checkbox" />
		  <span></span>
		  <span></span>
		  <span></span>
		  <ul id="menu">
		
		
    <router-link to="/">Home</router-link> <br>
      <router-link to="/About">About</router-link> <br>
          <router-link to="/Projects">Projects</router-link> <br>
            <router-link to="/Testimonials">Testimonials</router-link> <br>
              <router-link to="/Contact">Contact</router-link>
		  </ul>
		</div>
	  </nav>
    <router-view/>

<button @click="redirect">Redirect</button>
<button @click="back"> Go back</button>
<button @click="forward">Go Forward</button>

</template>

<script>
export default {
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

#light purple{
    color: rgba(199, 152, 226, 0.8);
}
:hover{
   color: #444 ;
 
}

nav .nav nav-pills{
    background-color: #6762a6;
}

body
{
  margin: 0;
  padding: 0;
}

#menuToggle
{
  display: block;
  position: relative;
  top: 50px;
  left: 50px;
  z-index: 1;
  -webkit-user-select: none;
  user-select: none;
}

#menuToggle a
{
  text-decoration: none;
  color: #6762a6; 
  transition: color 0.2s ease;
}

#menuToggle a:hover
{
  color: #c9c3e6;
}
.nav-link.active{
    color: #6762a6
}

#menuToggle input
{
  display: block;
  width: 40px;
  height: 32px;
  position: absolute;
  top: -7px;
  left: -5px;
  cursor: pointer;
  opacity: 0; /* hide this */
  z-index: 2; /* and place it over the hamburger */
  
  -webkit-touch-callout: none;
}

/*
 * Just a quick hamburger
 */
#menuToggle span
{
  display: block;
  width: 33px;
  height: 4px;
  margin-bottom: 5px;
  position: relative;
  background: #cdcdcd;
  border-radius: 3px;
  z-index: 1;
  transform-origin: 4px 0px;
  transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
              background 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
              opacity 0.55s ease;
}

#menuToggle span:first-child
{
  transform-origin: 0% 0%;
}

#menuToggle span:nth-last-child(2)
{
  transform-origin: 0% 100%;
}

/* 
 * Transform all the slices of hamburger
 * into a crossmark.
 */
#menuToggle input:checked ~ span
{
  opacity: 1;
  transform: rotate(45deg) translate(-2px, -1px);
  background: #5a5a5f;
}

/*
 * But let's hide the middle one.
 */
#menuToggle input:checked ~ span:nth-last-child(3)
{
  opacity: 0;
  transform: rotate(0deg) scale(0.2, 0.2);
}

/*
 * Ohyeah and the last one should go the other direction
 */
#menuToggle input:checked ~ span:nth-last-child(2)
{
  transform: rotate(-45deg) translate(0, -1px);
}

/*
 * Make this absolute positioned
 * at the top left of the screen
 */
#menu
{
  position: absolute;
  width: 300px;
  margin: -100px 0 0 -50px;
  padding: 50px;
  padding-top: 125px;
  height: 700px;
  background: #34333a;
  list-style-type: none;
  -webkit-font-smoothing: antialiased;
  /* to stop flickering of text in safari */
  
  transform-origin: 0% 0%;
  transform: translate(-100%, 0);
  
  transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0);
}

#menu li
{
  padding: 10px 0;
  font-size: 22px;
}

/*
 * And let's slide it in from the left
 */
#menuToggle input:checked ~ ul
{
  transform: none;
}
</style>
