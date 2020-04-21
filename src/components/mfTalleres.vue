<template>
  <div class="mfTalleres" id="mfTalleres">
    <div class="title">
      <h1>Comienza la aventura</h1>
    </div>
    <ul class="talleres">
      <li v-for="(item, index) in items" :key="index">
        <mf-talleres-item :data="item" />
      </li>
    </ul>
  </div>
</template>

<script>
import mfTalleresItem from '@/components/mfTalleresItem'
export default {
  name: 'mfTalleres',
  components: { mfTalleresItem },
  data() {
    return {
      items: [
        {
          name: 'Taller Básico',
          title: ' ',
          description: ' ',
          img: 'basico/img.png',
          logo: 'basico/logo.png'
        },
        {
          name: 'Taller Básico',
          title: ' ',
          description: ' ',
          img: 'basico/img.png',
          logo: 'basico/logo.png'
        },
        {
          name: 'Taller Básico',
          title: ' ',
          description: ' ',
          img: 'basico/img.png',
          logo: 'basico/logo.png'
        },
        {
          name: 'Taller Básico',
          title: ' ',
          description: ' ',
          img: 'basico/img.png',
          logo: 'basico/logo.png'
        }
      ]
    }
  }
}
</script>

<style scoped>
.mfTalleres {
  font-family: 'Encode Sans', sans-serif;
  width: 1366px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
}
.talleres {
  padding: 0;
  width: 98%;
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  align-items: center;
  justify-content: space-between;
}

.title {
  align-self: flex-start;
}
.title h1 {
  margin-top: 40px;
  margin-left: 40px;
}
</style>