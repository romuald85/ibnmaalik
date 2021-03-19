<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div> -->
    
  <router-view />
</template>
<script>
  export default {
    name: 'App',
    data() {
      return {
        
      }
    }
  }
</script>
<style>
  *{
    box-sizing: border-box;
  }

  html, body{
    height: 100%;
  }

  #app {
    font-family: Montserrat, Avenir, Helvetica, Arial, sans-serif;
    font-size: 18px;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }
</style>