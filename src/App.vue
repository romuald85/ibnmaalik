<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div> -->
    
  <router-view />
  <div id="footer">
    <Footer />
  </div>
</template>
<script>
  import Footer from '@/components/Footer.vue'
  export default {
    name: 'App',
    components: {
      Footer
    },
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
  #app {
    font-family: Montserrat, Avenir, Helvetica, Arial, sans-serif;
    font-size: 18px;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }

</style>