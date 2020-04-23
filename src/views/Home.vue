<template>
  <div class="home">
    <div class="home__content">
      <mf-hero />
      <div class="mf-talleres__section">
        <mf-talleres />
      </div>
      <div class="aprende-mas">
        <a href>Aprende a distancia >>>>>>></a>
      </div>
      <section class="foto-paseos__img">
        <img src="../assets/FOTOPASEO.png" alt="Fotopaseo" />
        <mf-button class="boton" :message="fotopaseo"></mf-button>
      </section>
      <section class="contacto">
        <img src="../assets/TELÉFONO.png" alt="cellphone" />
        <div class="contacto__info">
          <h2>
            Contáctate
            <br />con el Equipo
          </h2>
          <mf-button :message="contacto" class="contacto__boton"></mf-button>
        </div>
      </section>
    </div>
    <section class="ubicacion">
      <div class="encuentranos__info">
        <div class="encuentranos__container">
          <div class="encuentranos__banner">
            <div class="banner__content">
              <h3>Encuéntranos</h3>
              <p>
                Av. Pascual Orozco #2123 Col. la Cima
                <br />Frente a la deportiva, Chihuahua, Chih.
              </p>
            </div>
          </div>
          <div class="encuentranos__social">
            <div class="social__content">
              <a
                class="social__facebook"
                target="_blank"
                href="https://www.facebook.com/escuelamejoresfotos"
              >
                <img src="../assets/iconos/facebook.png" alt="facebook" />
              </a>
              <a
                class="social__instagram"
                target="_blank"
                href="https://www.instagram.com/escuelamejoresfotos/"
              >
                <img src="../assets/iconos/instagram.png" alt="facebook" />
              </a>
              <a class="social__tictok" target="_blank" href>
                <img src="../assets/iconos/tik-tok.png" alt="facebook" />
              </a>
            </div>
            <h3>@escuelamejoresfotos</h3>
          </div>
        </div>
        <div class="encuentranos__maps">
          <a
            target="_blank"
            href="https://www.google.com.mx/maps/place/Mejores+fotos/@28.6599499,-106.0896278,17z/data=!3m1!4b1!4m5!3m4!1s0x86ea436cb3187dc3:0x7cc52f838fdd58bc!8m2!3d28.6599452!4d-106.0874391"
          >
            <img src="../assets/mapa.png" alt="ubicacion" />
          </a>
        </div>
      </div>
      <div class="mejoresfotos">
        <h1>MEJORES FOTOS</h1>
      </div>
    </section>
  </div>
</template>

<script>
import mfHero from '@/components/mfHero'
import mfTalleres from '@/components/mfTalleres'
import mfButton from '@/components/mfButton'

export default {
  name: 'Home',
  components: {
    mfHero,
    mfTalleres,
    mfButton
  },
  data() {
    return {
      fotopaseo: {
        name: 'Conoce nuestra galería'
      },
      contacto: {
        name: 'Enviar Mensaje'
      }
    }
  }
}
</script>
<style>
.home {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.header {
  width: inherit;
}
.home__content {
  max-width: 1350px;
}
.aprende-mas {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 30px 0 50px 0;
}
.aprende-mas a {
  font-family: 'Encode Sans', sans-serif;
  color: #212d47;
  font-size: 20px;
  font-weight: bold;
  text-decoration: none;
  padding: 15px;
  width: 500px;
  text-align: center;
  border-radius: 25px;
  box-shadow: 0 0 10px 0 gray;
}
.foto-paseos__img {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.foto-paseos__img img {
  width: 90%;
  box-shadow: 0 0 10px 0 gray;
}
.foto-paseos__img .boton {
  position: relative;
  top: -50px;
  width: 400px;
  font-weight: bold;
  font-size: 24px;
}
.contacto {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  color: #045a4f;
}
.contacto__info {
  font-family: 'Encode Sans', sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.contacto img {
  margin-top: 20px;
  width: 30%;
}
.contacto__info h2 {
  text-align: center;
  font-size: 72px;
  font-weight: bold;
}
.contacto__boton {
  background: #045a4f;
  font-size: 24px;
  width: 200px;
  align-self: center;
}
.ubicacion {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: linear-gradient(white, #212d47);
}
.encuentranos__info {
  width: 1350px;
  display: flex;
}
.encuentranos__container {
  font-family: 'Encode Sans', sans-serif;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.encuentranos__banner {
  width: 600px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  text-align: center;
  padding: 0px 70px;
  margin-top: 200px;
  margin-left: 100px;
  border-radius: 100px;
  box-shadow: 0 0 10px gray;
  background: white;
}
.encuentranos__maps {
  position: relative;
  left: -400px;
}
.encuentranos__social {
  margin-left: 150px;
  color: white;
  display: flex;
  flex-direction: column;
}
.encuentranos__social h3 {
  font-size: 24px;
}
.social__content a img {
  width: 40px;
}
.social__content a {
  margin: 0 25px;
}
.encuentranos__social ul {
  list-style: none;
}
.mejoresfotos {
  font-family: 'Fira Sans', sans-serif;
  font-weight: bold;
  font-size: 18px;
  padding: 0;
  margin: 0;
  color: white;
}
</style>
