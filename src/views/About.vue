<template>

<h2>about</h2>



<!-- skills -->
    <div id="skillsContainer" class="container">
        <div class="row">
            <div class="col">
                  <div class="card">
                    <div class="face face1">
                        <div class="content">
                            <img src="https://i.postimg.cc/MpbPHXmw/html5.png">
                            <h3>Html</h3>
                        </div>
                    </div>
                    <div class="face face2">
                        <div class="content">
                            <p  class="display-6 text-muted">Skill level: Intermediate</p>
                              
                        </div>
                    </div>
                  </div>
            </div>
            <div class="col">
                <div class="card">
                  <div class="face face1">
                      <div class="content">
                          <img src="https://i.postimg.cc/TPMttf71/javascript.png">
                          <h3>Java-Script</h3>
                      </div>
                  </div>
                  <div class="face face2">
                      <div class="content">
                          <p  class="display-6 text-muted">Skill level: Beginner</p>
                      </div>
                  </div>
                </div>
            </div>
            <div class="col">
            
              <div class="card">
                <div class="face face1">
                    <div class="content">
                        <img src="https://i.postimg.cc/TYbmCmZj/mysql.png">
                        <h3>MySql</h3>
                    </div>
                </div>
                <div class="face face2">
                    <div class="content">
                        <p  class="display-6 text-muted">Skill level: Intermediate</p>
                    </div>
                </div>
          </div>
         </div>
        </div>
    </div>
    <div  id="skillsContainer" class="container">
      <div class="row">
          <div class="col">
                <div class="card">
                  <div class="face face1">
                      <div class="content">
                      <img id="css" src="https://i.postimg.cc/MZVKLDpG/css3.png">
                        <h3>Cascading Style Sheet</h3>
                      </div>
                  </div>
                  <div class="face face2">
                      <div class="content">
                          <p  class="display-6 text-muted">Skill level:  Beginner</p>
                      </div>
                  </div>
                </div>
          </div>
          <div class="col">
              <div class="card">
                <div class="face face1">
                    <div class="content">
                        <img src="https://i.postimg.cc/HxLsRDjD/bootstrap.png">
                        <h3>Bootstrap</h3>
                    </div>
                </div>
                <div class="face face2">
                    <div class="content">
                        <p  class="display-6 text-muted">Skill level: Intermediate</p>
                    </div>
                </div>
              </div>
          </div>
         
          
            <div class="card">
              <div class="face face1">
                  <div class="content">
                  <img src="https://i.postimg.cc/6qcsXTPM/github.png">
                    <h3>Github</h3>
                  </div>
              </div>
              <div class="face face2">
                  <div class="content">
                      <p  class="display-6 text-muted">Skill level: Intermediate</p>
                          <!-- <a href="#">Read More</a> -->
                  </div>
              </div>
        </div>
         <div class="card">
              <div class="face face1">
                  <div class="content">
                  <img src="https://i.postimg.cc/sg7FcVPH/4691448-dot-js-vue-icon.png">
                    <h3>Vue</h3>
                  </div>
              </div>
              <div class="face face2">
                  <div class="content">
                      <p  class="display-6 text-muted">Skill level: Intermediate</p>
                          <!-- <a href="#">Read More</a> -->
                  </div>
              </div>
        </div>
       
      </div>
  </div>


</template>

<script>



export default {
   components: {},
   
   methods: {},
}
</script>

<style>
.container{
  width: 1000px;
  position: relative;
  display: flex;
  justify-content: space-between;
  margin-top: 30px;
}
.row{
  margin-left: 100px;
}
.container .card{
  position: relative;
  cursor: pointer;
  /* margin-right: 50px; */
  margin-left: 45px;
  /* padding: 30px; */
}
.container .card .face{
  width: 300px;
  height: 200px;
  transition: 0.5s;
}
.container .card .face.face1{
  position: relative;
  background: #333;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
  transform: translateY(100px);
}
.container .card:hover .face.face1{
  background: #6762a6;
  transform: translateY(0);
}
.container .card .face.face1 .content{
  opacity: 0.2;
  transition: 0.5s;
}
.container .card:hover .face.face1 .content{
  opacity: 1;
}
.container .card .face.face1 .content img{
  max-width: 100px;
}
.container .card .face.face1 .content h3{
  margin: 10px 0 0;
  padding: 0;
  color: #fff;
  text-align: center;
  font-size: 1.5em;
}
.container .card .face.face2{
  position: relative;
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  box-sizing: border-box;
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.8);
  transform: translateY(-100px);
}
.container .card:hover .face.face2{
  transform: translateY(0);
}
.container .card .face.face2 .content p{
  margin: 0;
  padding: 0;
}
.container .card .face.face2 .content a{
  margin: 15px 0 0;
  display:  inline-block;
  text-decoration: none;
  font-weight: 900;
  color: #333;
  padding: 5px;
  border: 1px solid #333;
}
.container .card .face.face2 .content a:hover{
  background: #333;
  color: #fff;
}
::after .container .card .face.face1 .content{
  opacity: 1;
}
/* END */
</style>