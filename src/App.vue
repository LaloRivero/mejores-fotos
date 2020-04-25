<template>
  <div id="app">
    <mf-header class="header" v-if="basedOnWindowWidth" />
    <mf-burguer-menu v-else></mf-burguer-menu>
    <home />
  </div>
</template>

<script>
import mfHeader from '@/components/mfHeader'
import mfBurguerMenu from '@/components/burguerMenu'
import Home from '@/views/Home'
export default {
  data() {
    return {
      windowWidth: null
    }
  },
  components: { Home, mfHeader, mfBurguerMenu },
  created() {
    // window.addEventListener((this.windowWidth = window.innerWidth))
    this.windowWidth = window.innerWidth
  },
  computed: {
    basedOnWindowWidth() {
      if (this.windowWidth > 736) {
        return true
      }
      return false
    }
  }
}
</script>
<style>
@import url('./styles/media.css');
@import url('https://fonts.googleapis.com/css2?family=Fira+Sans:wght@400;500;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Encode+Sans:wght@400;500;700&family=Fira+Sans:wght@400;500;700&display=swap');
body {
  margin: 0;
}
.mf-button {
  height: 40px;
  padding: 10px 20px;
  background: #212d47;
  color: white;
  text-decoration: none;
  border-radius: 25px;
  cursor: pointer;
  display: flex;
  align-items: content;
  justify-content: center;
}
</style>
