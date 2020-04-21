<template>
  <div id="app">
    <home />
  </div>
</template>

<script>
import Home from '@/views/Home'
export default {
  data() {
    return {}
  },
  components: { Home }
}
</script>
<style>
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
