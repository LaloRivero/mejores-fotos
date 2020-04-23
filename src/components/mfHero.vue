<template>
  <div class="hero" id="hero">
    <div class="hero__container">
      <div class="hero__left-side">
        <h1>
          APRENDE EN
          <br />COMUNIDAD
        </h1>
      </div>
      <div class="hero__right-side">
        <img src="../assets/hero_img.png" alt="Video" />
        <div class="hero__buttons">
          <mf-button class="hero__boton" :message="conocenos"></mf-button>
          <mf-button class="hero__boton" :message="aprende"></mf-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import mfButton from '@/components/mfButton'

export default {
  name: 'mfHero',
  components: { mfButton },
  data() {
    return {
      conocenos: {
        name: 'Conócenos'
      },
      aprende: {
        name: 'Aprende'
      }
    }
  }
}
</script>

<style>
.hero {
  font-family: 'Encode Sans', sans-serif;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.hero__container {
  width: 100%;
  height: 700px;
  background: url('../assets/F-MF-WP.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: bottom;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.hero__left-side {
  width: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.hero__left-side h1 {
  margin-right: 65px;
  font-size: 50px;
  font-weight: bold;
  color: white;
}
.hero__right-side {
  width: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.hero__right-side img {
  width: 80%;
  padding: 15px;
  box-shadow: 0 0 15px 0 gray;
}
.hero__buttons {
  width: 90%;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
</style>
