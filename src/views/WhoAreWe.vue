<template>
    <div class="who-are-we">
        <Banner/>
        <MainWhoAreWe/>
    </div>
</template>
<script>
import Banner from '@/components/Banner.vue'
import MainWhoAreWe from '@/components/MainWhoAreWe.vue'

export default {
  name: 'WhoAreWe',
  components: {
    Banner, MainWhoAreWe
  }
}
</script>