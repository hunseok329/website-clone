<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->    
    <NavHeader/>
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import NavHeader from './components/NavHeader.vue'

export default {
  name: 'App',
  components: {
    NavHeader,
    HelloWorld
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
  /* margin-top: 60px; */
}
body {
  margin: 0;
}
</style>
