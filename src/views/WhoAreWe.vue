<template>
    <div class="who-are-we">
        <Navbar/>
        <Banner/>
        <MainWhoAreWe/>
        <Footer/>
    </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import Banner from '@/components/Banner.vue'
import MainWhoAreWe from '@/components/MainWhoAreWe.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'WhoAreWe',
  components: {
    Navbar,Footer, Banner, MainWhoAreWe
  }
}
</script>