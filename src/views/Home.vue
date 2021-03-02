<template>
  <div class="home">
    <Banner/>
    <MainHome/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Banner from '@/components/Banner.vue'
import MainHome from '@/components/MainHome.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld, Banner, MainHome
  }
}
</script>
