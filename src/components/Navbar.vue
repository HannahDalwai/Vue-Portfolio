<template>
    <!-- <div id="nav" role="navigation" class="nav nav-pills">
  </div> -->


  
		 <header id="header">
    <div class="d-flex flex-column">
<!-- HEADER IN NAV -->
      <div class="profile">
        <img src="https://i.postimg.cc/pTtYQqTn/fall-g93027d2b4-1920.jpg" alt="" class="img-fluid rounded-circle">
        <h1 class="text-light"><a href="index.html">Hannah</a></h1>
        <div class="social-links mt-3 text-center">
          <a href="#" class="github" data-bs-toggle="tooltip" data-bs-placement="bottom" title="Github"><i class='bx bxl-github'></i></a>
          <a href="#" class="netlify" data-bs-toggle="tooltip" data-bs-placement="bottom" title="Netlify"><i class='bx bxl-netlify'></i></a>
          <a href="#" class="linkedin" data-bs-toggle="tooltip" data-bs-placement="bottom" title="Linkedin"><i class='bx bxl-linkedin'></i></a>
          <a href="#" class="codepen" data-bs-toggle="tooltip" data-bs-placement="bottom" title="Codepen"><i class='bx bxl-codepen'></i></a>
        </div>
      </div>
<!-- NAVBAR -->
      <nav id="navbar" class="nav-menu navbar">
        <ul>
    <router-link to="/"><i class='bx bxs-home' ></i>  Home</router-link> <br>
      <router-link to="/About"><i class='bx bxs-info-circle'></i>  About</router-link> <br>
          <router-link to="/Projects"><i class='bx bx-book-content'></i>  Projects</router-link> <br>
            <router-link to="/Testimonials"><i class='bx bx-face'></i>  Testimonials</router-link> <br>
              <router-link to="/Contact"><i class='bx bxs-chat'></i>  Contact</router-link>
      
        </ul>
      </nav><!--END NAV -->
    </div>
  </header><!-- END HEADER -->

    <router-view/>
</template>

<script>
export default {

}
</script>

<style>
#header {
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  width: 300px;
  transition: all ease-in-out 0.5s;
  z-index: 9997;
  transition: all 0.5s;
  padding: 0 15px;
  background: #040b14;
  overflow-y: auto;
}
#header .profile img {
  margin: 15px auto;
  display: block;
  width: 120px;
  border: 4px solid #9B95BF;
}
#header .profile h1 {
  font-size: 24px;
  margin: 0;
  padding: 0;
  font-weight: 600;
  -moz-text-align-last: center;
  text-align-last: center;
  font-family: "Poppins", sans-serif;
}
#header .profile h1 a, #header .profile h1 a:hover {
  color: #fff;
  text-decoration: none;
}
#header .profile .social-links a {
  font-size: 18px;
  display: inline-block;
  background: #212431;
  color: #fff;
  line-height: 1;
  padding: 8px 0;
  margin-right: 4px;
  border-radius: 50%;
  text-align: center;
  width: 36px;
  height: 36px;
  transition: 0.3s;
}
#header .profile .social-links a:hover {
  background: #8e88b1;
  color: #fff;
  text-decoration: none;
}

#main {
  margin-left: 300px;
}

@media (max-width: 1199px) {
  #header {
    left: -300px;
  }

  #main {
    margin-left: 0;
  }
}
/*--------------------------------------------------------------
# Navigation Menu
--------------------------------------------------------------*/
/* Desktop Navigation */

.nav-menu {
  padding: 30px 0 0 0;
  margin-left:38px ;
}
.nav-menu * {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;

}
.nav-menu > ul > li {
  position: relative;
  white-space: nowrap;
  
}
.nav-menu a, .nav-menu a:focus {
  display: flex;
  align-items: center;
  color: #a8a9b4;
  padding: 12px 15px;
  margin-bottom: 8px;
  transition: 0.3s;
  font-size: 15px;
  

}
.nav-menu a i, .nav-menu a:focus i {
  font-size: 24px;
  padding-right: 8px;
  color: #6f7180;
}
.nav-menu a:hover, .nav-menu .active, .nav-menu .active:focus, .nav-menu li:hover > a {
  text-decoration: none;
  color: #fff;
}
.nav-menu a:hover i, .nav-menu .active i, .nav-menu .active:focus i, .nav-menu li:hover > a i {
  color: #9B95BF;
}

/* Mobile Navigation */
.mobile-nav-toggle {
  position: fixed;
  right: 15px;
  top: 15px;
  z-index: 9998;
  border: 0;
  font-size: 24px;
  transition: all 0.4s;
  outline: none !important;
  background-color: #9B95BF;
  color: #fff;
  width: 40px;
  height: 40px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  line-height: 0;
  border-radius: 50px;
  cursor: pointer;
}

.mobile-nav-active {
  overflow: hidden;
}
.mobile-nav-active #header {
  left: 0;
}

</style>