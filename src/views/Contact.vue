<template>
    <div class="register">
        <Navbar/>
        <MainContact/>
        <Footer/>
    </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import MainContact from '@/components/MainContact.vue'
import Footer from '@/components/Footer.vue'
export default {
    name: 'Contact',
    components: {
    Navbar, MainContact, Footer
  }
}
</script>
<style scoped>

</style>