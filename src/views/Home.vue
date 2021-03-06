<template>
  <div class="home">
    <Navbar/>
    <MainHome/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Navbar from '@/components/Navbar.vue'
import MainHome from '@/components/MainHome.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld, Navbar, MainHome
  }
}
</script>
