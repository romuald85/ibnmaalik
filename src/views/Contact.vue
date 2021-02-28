<template>
    <div class="register">
        <Navbar/>
        <Banner/>
        <MainContact/>
        <Footer/>
    </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import Banner from '@/components/Banner.vue'
import MainContact from '@/components/MainContact.vue'
import Footer from '@/components/Footer.vue'
export default {
    name: 'Contact',
    components: {
    Navbar,Footer, Banner, MainContact
  }
}
</script>
<style scoped>

</style>