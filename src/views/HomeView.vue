<template>
  <v-app id="home">
    <NavBar/>
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative;" class="mt-16">
              <h1 class="text-white">Holi</h1>
              <h1 class="text-white">Soy Edgar Xocoyotzin</h1>
              <span class="text-white">Ing.Gestión administración y arquitectura de software</span><br>
              <v-btn tile dark class="text-white" variant="outlined">Contactame</v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div style="position: absolute;z-index: 9999;bottom:0;
            margin-left:auto;margin-right:auto;left:0;right:0;
            text-align:center">
            <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999;" class="mt-16">
              <v-img src="../assets/perrito.jpg" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="../assets/iXRFBhFsx_1200x0__2.jpg" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h2 class="mt-16">About Me</h2>
              <div style="width:120px">
                <v-slider v-model="slider2" color="black" label="">
                </v-slider>
              </div>
              <h4 class="mt-n4"> Tengo X años haciendo donas</h4>
              <h4>y pasteles</h4>
              <p class="text-grey">Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima beatae ducimus assumenda, reiciendis aut nesciunt molestiae sunt! Ipsa rerum amet id distinctio, veniam quos soluta minima, itaque, ut vel sunt.</p>
              <br>
              <p class="text-gray">Lorem</p>
              <v-btn title dark color="green" class="mt-4">
                Descargar CV
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h1>Lo que hago.</h1>
        <div style="width: 120px; margin: 0 auto">
          <v-slider v-model="slider2" color="black" label=""></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-laptop" color="green" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Web Desing</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor, <br> 
                  sit amet consectetur adipisicing elit. <br>
                   Nostrum, quam cumque! 
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-hand-back-fist" color="green" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Web Desing</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor, <br> 
                  sit amet consectetur adipisicing elit. <br>
                   Nostrum, quam cumque! 
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-circle-check" color="green" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Web Desing</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor, <br> 
                  sit amet consectetur adipisicing elit. <br>
                   Nostrum, quam cumque! 
                </p>
              </div>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-container>
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '../components/NavBar.vue';

export default defineComponent({
  name: 'HomeView',
  setup() {
    return { 
      slider2: 50,
      items : [
        { img: "gatito.jpg"},
        { img: "perrito.jpg"},
      ]
    }
  },

  components: {
    NavBar
  },
});
</script>

<style scoped>
.v-container {
  padding-top: 16px 0;
}
.head {
  position: relative;
  text-align: center;
  padding:12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: rgb(0, 0, 0);
  transform: skew(0deg, 6deg);
}
.head:after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: rgb(0, 0, 0);
  transform: skew(0deg, -6deg);
}  
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 365px;
  height: 300px;
  background-color: green;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 0%;
}
.first{
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}
.child{
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
.imgHover{
  padding: 0 200px;
}
.pre{
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: aliceblue;
}
.hire{
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}

</style>
