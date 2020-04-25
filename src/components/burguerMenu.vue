<template>
  <div id="b-menu">
    <link rel="icon" type="image/png" href="./images/fav icon.png" />
    <nav class="nav-movile-container">
      <a @click="event_menu">
        <i class="icon-menu burger-button"></i>
      </a>
      <a href class="img-logo-xl">
        <img src="../assets/Logotipo-blanco-Mefo.png" alt />
      </a>
    </nav>
    <transition name="fade">
      <ul v-show="hide_show_menu" class="menu">
        <li>
          <a href="/">Talleres</a>
        </li>
        <li>
          <a href="/">Conócenos</a>
        </li>
        <li>
          <a href="/">Comunidad</a>
        </li>
        <li>
          <a href="/">Blog</a>
        </li>
        <li>
          <a href="/">Aprende a Distancia</a>
        </li>
      </ul>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'BurgerMenu',
  data() {
    return {
      hide_show_menu: false
    }
  },
  methods: {
    event_menu() {
      return (this.hide_show_menu = !this.hide_show_menu)
    }
  }
}
</script>

<style>
@font-face {
  font-family: 'icomoon';
  src: url('../fonts/icomoon.eot?8f0wr6');
  src: url('../fonts/icomoon.eot?8f0wr6#iefix') format('embedded-opentype'),
    url('../fonts/icomoon.ttf') format('truetype'),
    url('../fonts/icomoon.woff') format('woff'),
    url('../fonts/icomoon.svg?8f0wr6#icomoon') format('svg');
  font-weight: normal;
  font-style: normal;
  font-display: block;
}

[class^='icon-'],
[class*=' icon-'] {
  /* use !important to prevent issues with browser extensions that change fonts */
  font-family: 'icomoon' !important;
  /* speak: none; */
  font-style: normal;
  font-weight: normal;
  font-variant: normal;
  text-transform: none;
  line-height: 1;

  /* Better Font Rendering =========== */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.icon-menu:before {
  content: '\e900';
}
.burger-button {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: rgba(33, 45, 71, 0.8);
  line-height: 40px;
  text-align: center;
  position: relative;
  z-index: 10;
  /* left: 5px;
  top: 5px; */
  color: white;
  cursor: pointer;
  margin-left: 15px;
}
.menu {
  font-family: 'Encode Sans', sans-serif;
  margin: 0;
  position: fixed;
  background-color: rgba(33, 45, 71, 0.9);
  z-index: 9;
  top: 0;
  left: 0vw;
  bottom: 0;
  width: 70vw;
  /* height: 100vh; */
  display: flex;
  flex-direction: column;
  align-items: left;
  justify-content: flex-start;
  transition: 0.5s;
  padding-top: 100px;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
.menu li {
  list-style: none;
  padding: 20px;
}
.menu li a {
  color: white;
  text-decoration: none;
  font-size: 24px;
}
.menu li a:hover {
  font-size: 26px;
}
.nav-movile-container {
  width: 100%;
  height: 50px;
  background: #212d47;
  display: flex;
  align-items: center;
}
.img-logo-xl {
  display: flex;
  align-items: center;
  margin-left: 15px;
}
.img-logo-xl img {
  height: 40px;
}
</style>