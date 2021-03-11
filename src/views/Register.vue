<template>
    <div class="register">
        <Navbar/>
        <MainRegister/>
        <Footer/>
    </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import MainRegister from '@/components/MainRegister.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Register',
  components: {
    Navbar, MainRegister, Footer
  }
}
</script>