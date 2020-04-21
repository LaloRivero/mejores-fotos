<template>
  <div class="mf-talleres-item">
    <div class="container" @mouseover="displayText" @mouseleave="noDisplayText">
      <div class="content">
        <img class="item-logo" :src="require(`@/assets/${data.logo}`)" alt />
        <div class="img__container">
          <div v-show="displayDescriptionText" class="active">
            <div class="overlay"></div>
            <div class="active__info">
              <h4>En qué consiste el {{ data.name }}</h4>
              <p>
                Lorem, ipsum dolor sit amet consectetur adipisicing elit. Obcaecati
                itaque recusandae tenetur asperiores accusantium, alias molestiae!
                molestiae! molestiae! molestiae! Expedita quod doloremque non
                provident nemo laudantium natus eius, consectetur maiores incidunt
                repellendus?
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

<style scoped>
.container {
  width: 320px;
  height: auto;
  margin: 10px 0;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  overflow: hidden;
  border-radius: 7px;
  box-shadow: 0 0 10px 0 gray;
}
.content {
  padding: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.img__curso {
  width: 100%;
  border-radius: 5px;
}
.active {
  position: relative;
}
.overlay {
  width: 300px;
  height: 460px;
  position: absolute;
  background: rgba(161, 0, 0, 0.479);
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
}
</style>