<template>
  <!--NAVBAR  -->
  <MyNavbar></MyNavbar>

  <div class="intro-graphic">
    <div class="hello-box">

    </div>
    <div class="box2">

    </div>
    <div class="box3">

    </div>

    <div class="im-box">

    </div>
    <div class="box5">

    </div>
    <div class="box6">

    </div>

    <div class="mike-box">

    </div>
    <div class="box8">

    </div>
    <div class="box9">

    </div>
  </div>

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

.intro-graphic {
  padding: 25px;
  padding-left: 150px;
  display: flex;
  gap: 10px;
}

.hello-box {
  width: 700px;
  height: 200px;
  background-color: #fcba03;
}

.box2 {
  width: 500px;
  height: 200px;
  background-color: #fcba03;
}

.box3 {
  width: 400px;
  height: 200px;
  background-color: #fcba03;
}
</style>
