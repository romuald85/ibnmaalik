<template>
    <div class="register">
        <Navbar/>
        <Banner/>
        <MainRegister/>
        <Footer/>
    </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import Banner from '@/components/Banner.vue'
import MainRegister from '@/components/MainRegister.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Register',
  components: {
    Navbar,Footer, Banner, MainRegister
  }
}
</script>