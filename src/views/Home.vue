<template>
  <div class="home">
    <Navbar/>
    <Banner/>
    <MainHome/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Navbar from '@/components/Navbar.vue'
import Banner from '@/components/Banner.vue'
import MainHome from '@/components/MainHome.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld, Navbar, Banner, MainHome, Footer
  }
}
</script>
