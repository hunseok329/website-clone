<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->    
    <NavHeader/>
    <CommunityHome/>
    <StoreHome/>
  </div>
</template>

<script>
import NavHeader from './components/NavHeader.vue'
import CommunityHome from './components/community/CommunityHome.vue'
// import StoreHome from './components/store/StoreHome.vue'

export default {
  name: 'App',
  components: {
    NavHeader,
    CommunityHome,
    // StoreHome
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  /* margin-top: 60px; */
}
body {
  margin: 0;
}
</style>
