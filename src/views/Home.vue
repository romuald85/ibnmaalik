<template>
  <div class="home bg-light">
    <Navbar/>
    <MainHome/>
    <MainPrograms/>
    <MainWhoAreWe/>
    <MainBackground/>
    <MainBooks/>
    <!-- <Footer/> -->
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Navbar from '@/components/Navbar.vue'
import MainHome from '@/components/MainHome.vue'
import MainPrograms from '@/components/MainPrograms.vue'
import MainWhoAreWe from '@/components/MainWhoAreWe.vue'
import MainBackground from '@/components/MainBackground.vue'
import MainBooks from '@/components/MainBooks.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld, Navbar, MainHome, MainPrograms, MainWhoAreWe, MainBackground, MainBooks, Footer
  }
}
</script>
