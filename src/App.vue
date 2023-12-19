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
        <img src="../src/assets/four-circles.png" :class="{ 'rotate2': rotateSmallCircles2, 'show2': showImage2 }" class="four-circles2" @click="rotateFourCircles2"/>
      </div>
    </div>

    <div class="row2">
      <div class="box5">
        <div class="square1"></div>
        <div class="square2"></div>
      </div>
      <div class="im-box">
        <div :class="{ 'zoom-spin': loaded }" class="im">I'm</div>
      </div>
      <div class="box6">
        <img src="../src/assets/green-circle.png" :class="{ 'rotate1': rotateOnLoad, 'show': showImage }" class="green-circle1" @click="rotateCircles"/>
        <img src="../src/assets/green-circle.png" :class="{ 'rotate2': rotateOnLoad, 'show': showImage }" class="green-circle2" @click="rotateCircles"/>
      </div>
    </div>

    <div class="row3">
      <div class="box9">
        <img src="../src/assets/four-circles.png" :class="{ 'rotate1': rotateSmallCircles, 'show2': showImage2 }" class="four-circles" @click="rotateFourCircles"/>
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
      // Animation variables
      loaded: false,
      rotateOnLoad: false,
      rotateSmallCircles: false,
      rotateSmallCircles2: false,
      showImage: false,
      showImage2: false
    }
  },

  mounted() {
    setTimeout(() => {
      this.loaded = true
      this.rotateOnLoad = true
      this.rotateSmallCircles = true
      this.rotateSmallCircles2 = true
      this.showImage = true
      this.showImage2 = true
    }, 500)
  },

  methods: {
    rotateCircles() {
      this.rotateOnLoad = !this.rotateOnLoad
    },
    rotateFourCircles() {
      this.rotateSmallCircles = !this.rotateSmallCircles
    },
    rotateFourCircles2() {
      this.rotateSmallCircles2 = !this.rotateSmallCircles2
    }
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

/*********** ROW 1 ************/
.row1 {
  padding-bottom: 15px;
  display: flex;
  gap: 15px;
}

.hello-box {
  width: 700px;
  height: 25vh;
  background-color: #6fd1a0;
  align-items: center;
  justify-content: center;
  display: flex;
}

.hello {
  opacity: 0;
  transform: translateX(-100px);
  text-size-adjust: auto;
  transition: transform 0.5s ease;
  font-size: 20vh;
}

.slide-in {
  opacity: 1;
  transform: translateX(0px);
}

.box2 {
  width: 600px;
  height: 25vh;
  background-color: #e681bb;
}

.box3 {
  width: 300px;
  height: 25vh;
  background-color: #84d1e3;
  align-items: center;
  justify-content: center;
  display: flex;
}

.four-circles2 {
  opacity: 0;
  width: 50%;
  height: auto;
  padding: 4%;
  transition: transform 2s ease, opacity 0.5s ease;
}



/*********** ROW 2 ************/
.row2 {
  padding-bottom: 15px;
  display: flex;
  gap: 15px;
}

.im-box {
  width: 700px;
  height: 25vh;
  background-color: #fcba03;
  font-size: 20vh;
  align-items: center;
  justify-content: center;
  display: flex;
}

.im {
  opacity: 0;
  text-size-adjust: auto;
  max-width: 100%;
  white-space: nowrap;
  overflow: hidden;
  animation: zoomSpinAnimation 1s forwards;
}

@keyframes zoomSpinAnimation {
  0% {
    transform: scale(0) rotate(0deg);
  }

  100% {
    transform: scale(1) rotate(360deg);
    opacity: 1;
  }
}

.box5 {
  width: 450px;
  height: 25vh;
  background-color: #84d1e3;
  align-items: center;
  justify-content: center;
  display: flex;
}

.box6{
  width: 450px;
  height: 25vh;
  background-color: #ab78c4;
  align-items: center;
  justify-content: center;
  display: flex;
}

.green-circle1 {
  opacity: 0;
  width: 40%;
  height: auto;
  padding: 4%;
  rotate: 5deg;
  transition: transform 3s ease, opacity 0.5s ease;
}

.green-circle2 {
  opacity: 0;
  width: 40%;
  height: auto;
  padding: 4%;
  rotate: 185deg;
  transition: transform 2s ease, opacity 0.5s ease;
}

.rotate1 {
  transform: rotate(360deg);
}
.rotate2 {
  transform: rotate(-360deg);
}
.show {
  opacity: 1;
}

.square1 {
  width: 30%;
  height: 15vh;
  background-color: #ab78c4;
  display: flex;
}
.square2 {
  width: 30%;
  height: 15vh;
  background-color: #ab78c4;
  margin-left: 70px;
}




/*********** ROW 3 ************/
.row3 {
  padding-bottom: 15px;
  display: flex;
  gap: 15px;
}

.box9 {
  width: 300px;
  height: 25vh;
  background-color: #ab78c4;
  align-items: center;
  justify-content: center;
  display: flex;
}

.four-circles {
  opacity: 0;
  width: 50%;
  height: auto;
  padding: 4%;
  transition: transform 3s ease, opacity 0.5s ease;
}
.show2 {
  opacity: 1;
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
