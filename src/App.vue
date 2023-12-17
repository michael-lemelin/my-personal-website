<template>
  <AboutMe></AboutMe>
  <MyProjects></MyProjects>
</template>

<script>
import AboutMe from './components/AboutMe.vue'
import MyProjects from './components/MyProjects.vue'

export default {
  name: 'App',
  components: {
    AboutMe,
    MyProjects,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
