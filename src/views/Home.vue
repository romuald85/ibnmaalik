<template>
  <div class="home">
    <Navbar/>
    <MainHome/>
    <MainPrograms/>
    <!-- <Footer/> -->
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Navbar from '@/components/Navbar.vue'
import MainHome from '@/components/MainHome.vue'
import MainPrograms from '@/components/MainPrograms.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld, Navbar, MainHome, MainPrograms, Footer
  }
}
</script>
