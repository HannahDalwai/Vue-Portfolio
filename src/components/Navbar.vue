<template>
 <i class="mobile-nav" @click="openNav()"><i class='bx bx-menu'></i></i>

<!-- NAVBAR -->
            <nav id="navbar" class="nav-menu navbar">
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
                  <ul>
                    <li> <router-link to="/"><i class='bx bxs-home' ></i>  Home</router-link>   </li>
                    <li><router-link to="/About"><i class='bx bxs-info-circle'></i>  About</router-link></li>
                    <li>  <router-link to="/Projects"><i class='bx bx-book-content'></i>  Projects</router-link> </li>
                    <li>  <router-link to="/Testimonials"><i class='bx bx-user'></i> Testimonials</router-link> </li>
                    <li>   <router-link to="/Contact"><i class='bx bxs-chat'></i>  Contact</router-link> </li>
                  </ul>
            </nav>

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

#navbar{
  position: fixed;
}

nav {
  position: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  background: #222;
  width: 280px;
  height: 700px;
  transition: all 0.1s linear;
  padding: 30px 0 0 0;
}
/* OTHER NAV STYLING */


nav * {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav > ul > li {
  position: relative;
  white-space: nowrap;
}
nav a, nav a:focus {

  align-items: center;
  color: #a8a9b4;
  padding: 12px 15px;
  margin-bottom: 8px;
  transition: 0.3s;
  font-size: 15px;
}
nav a i, nav a:focus i {
  font-size: 24px;
  padding-right: 8px;
  color: #6f7180;
}
nav a:hover, nav .active, nav .active:focus, nav li:hover > a {
  text-decoration: none;
  color: #fff;
}
nav a:hover i, .nav .active i, nav .active:focus i, nav li:hover > a i {
  color: white;
}

/* RESPONSIVE nav */
.mobile-nav {
  position: fixed;
  top: 20px;
  right: 20px;
  display: none;
}

@media screen and (max-width: 900px) {
  nav {
    left: -100%;
  }
  nav.active {
    left: 0;
  }
  main {
    margin-left: 0;
  }
  .mobile-nav {
  position: fixed;
  right: 15px;
  top: 15px;
  z-index: 9998;
  border: 0;
  font-size: 24px;
  transition: all 0.4s;
  outline: none !important;
  background-color: #631C48;
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
}

 /* PROFILE IN NAV */
.profile img {
    margin: 15px 20px;
    display: block;
    width: 120px;
    border: 4px solid #631C48;
  }

.profile h1 {
  font-size: 24px;
  margin: 0;
  padding: 0;
  font-weight: 600;
  -moz-text-align-last: center;
  text-align-last: center;
 
}
.profile h1 a,.profile h1 a:hover {
  color: #fff;
  text-decoration: none;
}
.profile .social-links a {
  text-decoration:none;
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
.profile .social-links a:hover {
  background: #631C48;
  color: #fff;
  text-decoration: none;
} 
</style>