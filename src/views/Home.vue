<template>
  <div class="home">
    <mf-header />
    <mf-hero />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import mfHeader from '@/components/mfHeader'
import mfHero from '@/components/mfHero'

export default {
  name: 'Home',
  components: {
    // HelloWorld,
    mfHeader,
    mfHero
  }
}
</script>
