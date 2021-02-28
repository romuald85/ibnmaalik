<template>
    <div class="register">
        <Navbar/>
        <Banner/>
        <MainTerms/>
        <Footer/>
    </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import Banner from '@/components/Banner.vue'
import MainTerms from '@/components/MainTerms.vue'
import Footer from '@/components/Footer.vue'
export default {
    name: 'Contact',
    components: {
    Navbar,Footer, Banner, MainTerms
  }
}
</script>
<style scoped>

</style>