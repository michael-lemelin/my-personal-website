<template>
  <!--NAVBAR  -->
  <MyNavbar></MyNavbar>

  <!-- ABOUT ME -->
  <AboutMe></AboutMe>

  <!-- MY PROJECTS -->
  <MyProjects></MyProjects>
</template>

<script>
import MyNavbar from './components/MyNavbar.vue'
import AboutMe from './components/AboutMe.vue'
import MyProjects from './components/MyProjects.vue'

export default {
  name: 'App',
  components: {
    MyNavbar,
    AboutMe,
    MyProjects,
  }
}
</script>

<style>
@font-face {
  font-family: 'CustomFont';
  src: url('@/assets/Fonts/static/CairoPlay-Light.ttf') format('ttf');
}

body {
  background-color: #101112;
  color: white;
  margin: 0;
  padding: 0;
}
</style>
