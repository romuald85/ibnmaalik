<template>
    <div class="register">
        <Banner/>
        <Navbar/>
        <MainTerms/>
        <Footer/>
    </div>
</template>
<script>
import Banner from '@/components/Banner.vue'
import Navbar from '@/components/Navbar.vue'
import MainTerms from '@/components/MainTerms.vue'
import Footer from '@/components/Footer.vue'
export default {
    name: 'Contact',
    components: {
    Banner, Navbar, MainTerms, Footer
  }
}
</script>
<style scoped>

</style>