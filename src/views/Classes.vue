<template>
    <div class="classes">
        <Banner/>
        <MainClasses/>
    </div>
</template>
<script>
import Banner from '@/components/Banner.vue'
import MainClasses from '@/components/MainClasses.vue'

export default {
    name: 'Classes',
    components: {Banner,  MainClasses}
}
</script>
<style scoped>

</style>