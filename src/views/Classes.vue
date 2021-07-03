<template>
    <div class="classes">
        <Banner/>
        <Navbar/>
        <MainClasses/>
        <Footer/>
    </div>
</template>
<script>
import Banner from '@/components/Banner.vue'
import Navbar from '@/components/Navbar.vue'
import MainClasses from '@/components/MainClasses.vue'
import Footer from '@/components/Footer.vue'
export default {
    name: 'Classes',
    components: {Banner, Navbar, MainClasses, Footer}
}
</script>
<style scoped>

</style>