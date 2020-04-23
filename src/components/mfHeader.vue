<template>
  <div>
    <div class="mf-header">
      <div class="header__container">
        <a href="/" class="header__logo">
          <img src="../assets/isotipo-blanco-mefo.png" alt="Mejores fotos" class="logo__img" />
        </a>
        <nav class="header__nav">
          <ul class="nav__conteiner">
            <li class="li_pipes">
              <a href="/">Talleres</a>
            </li>
            <li class="li_pipes">
              <a href="/">Conócenos</a>
            </li>
            <li class="li_pipes">
              <a href="/">Comunidad</a>
            </li>
            <li class="li_pipes">
              <a href="/">Blog</a>
            </li>
            <li class="li_pipes no_pipe">
              <a href="/">Aprende a Distancia</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'mfHeader'
}
</script>

<style>
.mf-header {
  width: 100%;
  font-family: 'Fira Sans', sans-serif;
  background: #212d47;
  display: flex;
  justify-content: center;
  align-items: center;
}
.header__container {
  width: 1350px;
  background-color: #212d47;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.nav__conteiner {
  width: auto;
  margin-right: 20px;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
.nav__conteiner li {
  margin: 0 10px;
  list-style: none;
}
.li_pipes {
  height: 25px;
  padding-right: 15px;
  border-right: 1px solid white;
  display: flex;
  align-items: center;
  justify-content: center;
}
.no_pipe {
  border: none;
}
.nav__conteiner li a {
  color: white;
  text-decoration: none;
}
.nav__conteiner li a:hover {
  padding-bottom: 5px;
  border-bottom: 2px solid white;
}
.header__logo {
  height: 60px;
  margin-left: 20px;
  display: block;
  display: flex;
  align-items: center;
  justify-content: center;
}
.logo__img {
  display: block;
  height: 40px;
  margin: 0;
  padding: 0;
}
@media screen and (max-width: 768) {
  * {
    color: red;
  }
  .nav__conteiner li {
    margin: 0 5px !important;
  }
  .li_pipes {
    padding-right: 10px;
  }
}
</style>
