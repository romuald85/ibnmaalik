<template>
    <div class="register">
        <Banner/>
        <MainContact/>
    </div>
</template>
<script>
import Banner from '@/components/Banner.vue'
import MainContact from '@/components/MainContact.vue'
export default {
    name: 'Contact',
    components: {
    Banner, MainContact
  }
}
</script>
<style scoped>

</style>