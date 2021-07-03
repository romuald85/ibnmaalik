<template>
    <div class="who-are-we">
        <Banner/>
        <Navbar/>
        <MainWhoAreWe/>
        <Footer/>
    </div>
</template>
<script>
import Banner from '@/components/Banner.vue'
import Navbar from '@/components/Navbar.vue'
import MainWhoAreWe from '@/components/MainWhoAreWe.vue'
import Footer from '@/components/Footer.vue'
export default {
  name: 'WhoAreWe',
  components: {
    Banner, Navbar, MainWhoAreWe, Footer
  }
}
</script>