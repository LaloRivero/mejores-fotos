<template>
  <div class="mf-talleres-item">
    <div class="container" @mouseover="displayText" @mouseleave="noDisplayText">
      <div class="content">
        <img class="item-logo" :src="require(`@/assets/${data.logo}`)" alt />
        <div class="img__container">
          <div v-show="displayDescriptionText" class="active">
            <div v-if="data.color === 'amarillo'" class="overlay__amarillo"></div>
            <div v-else-if="data.color === 'azul'" class="overlay__azul"></div>
            <div v-else-if="data.color === 'morado'" class="overlay__morado"></div>
            <div v-else class="overlay"></div>
            <div class="active__info">
              <h4>En qué consiste el {{ data.name }}</h4>
              <p>
                Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                Obcaecati itaque recusandae tenetur asperiores accusantium,
                alias molestiae! molestiae! molestiae! molestiae! Expedita quod
                doloremque non provident nemo laudantium natus eius, consectetur
                maiores incidunt repellendus?
              </p>
            </div>
          </div>
          <img class="img__curso" :src="require(`@/assets/${data.img}`)" :alt="data.name" />
        </div>
        <mf-button class="button" :message="itemMessage"></mf-button>
      </div>
    </div>
  </div>
</template>

<script>
import mfButton from '@/components/mfButton'
export default {
  name: 'mfTalleresItem',
  props: {
    data: {}
  },
  components: { mfButton },
  data() {
    return {
      itemMessage: {
        name: 'Entrar'
      },
      displayDescriptionText: false
    }
  },
  methods: {
    displayText() {
      this.displayDescriptionText = true
    },
    noDisplayText() {
      this.displayDescriptionText = false
    }
  }
}
</script>

<style>
.container {
  width: 300px;
  height: auto;
  margin: 10px 0;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  overflow: hidden;
  border-radius: 7px;
  box-shadow: 0 0 10px 0 gray;
  background-color: white;
}
.content {
  padding: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.img__curso {
  width: 260px;
  border-radius: 5px;
}
.active {
  position: relative;
}
.overlay {
  width: 260px;
  height: 398.667px;
  position: absolute;
  background: rgba(161, 0, 0, 0.479);
  border-radius: 5px;
}
.overlay__amarillo {
  width: 260px;
  height: 398.667px;
  position: absolute;
  background: rgba(230, 166, 32, 0.4);
  border-radius: 5px;
}
.overlay__azul {
  width: 260px;
  height: 398.667px;
  position: absolute;
  background: rgba(27, 37, 54, 0.4);
  border-radius: 5px;
}
.overlay__morado {
  width: 260px;
  height: 398.667px;
  position: absolute;
  background: rgba(119, 0, 255, 0.4);
  border-radius: 5px;
}
.active__info {
  padding: 15px;
  color: white;
  position: absolute;
}
.item-logo {
  width: 150px;
  margin-bottom: 10px;
}
.button {
  width: 80%;
  margin: 5px;
}
</style>
