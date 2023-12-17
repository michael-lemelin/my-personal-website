<template>
  <!--NAVBAR  -->
  <MyNavbar></MyNavbar>

  <div class="intro-graphic">

    <div class="row1">
      <div class="hello-box">

      </div>
      <div class="box2">

      </div>
      <div class="box3">

      </div>
    </div>

    <div class="row2">
      <div class="im-box">

      </div>
      <div class="box5">

      </div>
      <div class="box6">

      </div>
    </div>

    <div class="row3">
      <div class="mike-box">

      </div>
      <div class="box8">

      </div>
      <div class="box9">

      </div>
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
  padding-left: 7%;
  padding-right: 7%;
  margin-top: 100px;
}

.row1 {
  padding-bottom: 15px;
  display: flex;
  gap: 15px;
}

.hello-box {
  width: 700px;
  height: 25vh;
  background-color: #6fd1a0;
}

.box2 {
  width: 500px;
  height: 25vh;
  background-color: #e681bb;
}

.box3 {
  width: 400px;
  height: 25vh;
  background-color: #84d1e3;
}

.row2 {
  padding-bottom: 15px;
  display: flex;
  gap: 15px;
}

.im-box {
  width: 450px;
  height: 25vh;
  background-color: #84d1e3;
}

.box5 {
  width: 700px;
  height: 25vh;
  background-color: #fcba03;
}

.box6{
  width: 450px;
  height: 25vh;
  background-color: #ab78c4;
}

.row3 {
  padding-bottom: 15px;
  display: flex;
  gap: 15px;
}

.mike-box {
  width: 300px;
  height: 25vh;
  background-color: #ab78c4;
}

.box8 {
  width: 650px;
  height: 25vh;
  background-color: #e681bb;
}

.box9 {
  width: 650px;
  height: 25vh;
  background-color: #6fd1a0;
}
</style>
