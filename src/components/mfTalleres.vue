<template>
  <div class="mfTalleres" id="mfTalleres">
    <div class="talleres__container">
      <div class="title">
        <h1>Comienza la aventura</h1>
      </div>
      <ul class="talleres">
        <li v-for="(item, index) in items" :key="index">
          <mf-talleres-item :data="item" class="taller__item" />
        </li>
      </ul>
      <mf-talleres-item :data="sendItem" class="item__taller"></mf-talleres-item>
      <a class="arrow-left__container" @click="moveBackwardsItem">
        <img class="talleres__arrow" src="../assets/arrow.png" alt="arrow" />
      </a>
      <a class="arrow-right__container" @click="moveFowardsItem">
        <img class="talleres__arrow-right" src="../assets/arrow-right.png" alt="arrow" />
      </a>
    </div>
  </div>
</template>

<script>
import mfTalleresItem from '@/components/mfTalleresItem'
export default {
  name: 'mfTalleres',
  components: { mfTalleresItem },
  data() {
    return {
      index: 0,
      sendItem: {},
      items: [
        {
          name: 'Taller Básico',
          title: ' ',
          description: ' ',
          img: 'basico/img.png',
          logo: 'basico/logo.png',
          color: 'amarillo'
        },
        {
          name: 'Taller Intermedio',
          title: ' ',
          description: ' ',
          img: 'basico/img.png',
          logo: 'basico/logo.png',
          color: 'azul'
        },
        {
          name: 'Taller Avanzado',
          title: ' ',
          description: ' ',
          img: 'basico/img.png',
          logo: 'basico/logo.png',
          color: 'morado'
        },
        {
          name: 'Taller Especializados',
          title: ' ',
          description: ' ',
          img: 'especial/img.png',
          logo: 'especial/logo.png'
        }
      ]
    }
  },
  mounted: function() {
    this.sendItem = this.items[0]
  },
  methods: {
    moveFowardsItem() {
      if (this.index < this.items.length) {
        this.index = this.index + 1
        this.sendItem = this.items[this.index]
      }
    },
    moveBackwardsItem() {
      if (this.index >= 0) {
        this.index = this.index - 1
        this.sendItem = this.items[this.index]
      }
    }
  }
}
</script>

<style>
.talleres__container {
  font-family: 'Encode Sans', sans-serif;
  width: 1350px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
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
.taller__item {
  position: relative;
  z-index: 10;
}
.title {
  align-self: flex-start;
}
.title h1 {
  margin-top: 40px;
  margin-left: 40px;
}
.talleres__arrow {
  position: absolute;
  top: 50%;
  left: 10px;
  z-index: 2;
  width: 40px;
}
.talleres__arrow-right {
  position: absolute;
  top: 50%;
  right: 10px;
  z-index: 2;
  width: 40px;
}
.item__taller {
  display: none;
}
.talleres__container a {
  cursor: pointer;
}
</style>
