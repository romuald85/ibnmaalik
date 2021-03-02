<template>
    <div class="register">
        <Banner/>
        <MainRegister/>
    </div>
</template>
<script>
import Banner from '@/components/Banner.vue'
import MainRegister from '@/components/MainRegister.vue'

export default {
  name: 'Register',
  components: {
    Banner, MainRegister
  }
}
</script>