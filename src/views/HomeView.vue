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
    </v-container>
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '../components/NavBar.vue';

export default defineComponent({
  name: 'HomeView',

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

</style>
