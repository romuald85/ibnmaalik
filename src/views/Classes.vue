<template>
    <div class="classes">
        <Navbar/>
        <Banner/>
        <MainClasses/>
        <Footer/>
    </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import Banner from '@/components/Banner.vue'
import MainClasses from '@/components/MainClasses.vue'
import Footer from '@/components/Footer.vue'

export default {
    name: 'Classes',
    components: {Navbar, Banner, Footer, MainClasses}
}
</script>
<style scoped>

</style>