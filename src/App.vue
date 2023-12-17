<template>
  <!--NAVBAR  -->
  <MyNavbar></MyNavbar>

  <div class="intro-graphic">

    <div class="row1">
      <div class="hello-box">
        <h1 :class="{ 'slide-in': loaded }" class="hello">Hello,</h1>
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
      <div class="box9">
        
      </div>
      <div class="box8">
        
      </div>
      <div class="mike-box">
        <h1 :class="{ 'pop-animation': loaded }" class="mike">Mike!</h1>
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
  },

  data() {
    return {
      loaded: false
    }
  },

  mounted() {
    setTimeout(() => {
      this.loaded = true
    }, 1000)
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
  font-family: 'CustomFont', 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.intro-graphic {
  padding: 25px;
  padding-left: 7%;
  padding-right: 7%;
  margin-top: 100px;
  color: #101112;
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
  font-size: 10vh;
  align-items: center;
  justify-content: center;
  display: flex;
}

.hello {
  opacity: 0;
  transform: translateX(-100px);
  text-size-adjust: auto;
  transition: transform 0.5s ease;
}

.slide-in {
  opacity: 1;
  transform: translateX(0px);
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

.box9 {
  width: 300px;
  height: 25vh;
  background-color: #ab78c4;
}

.box8 {
  width: 650px;
  height: 25vh;
  background-color: #e681bb;
}




.mike-box {
  width: 650px;
  height: 25vh;
  background-color: #6fd1a0;
  align-items: center;
  justify-content: center;
  display: flex;
  font-size: 10vh;
}

.mike {
  opacity: 0;
  text-size-adjust: auto;
  max-width: 100%;
  white-space: nowrap;
  overflow: hidden;
}

.pop-animation {
  animation: popAnimation 0.5s cubic-bezier(0.68, -0.55, 0.27, 1.55) forwards;
}

@keyframes popAnimation {
  0% {
    transform: scale(0);
  }
  80% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}
</style>
