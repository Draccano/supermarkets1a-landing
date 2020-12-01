<template>
  <main class="home">
    <!--BIG MAIN HERO-->
    <section class="landing-hero">
      <b-jumbotron
        fluid
        header="¡Haz tus compras sin salir de casa!"
        lead="Pide todo lo que necesites con nuestro nuevo servicio de delivery, rápido, fácil y sin salir de casa."
      >
        <default-button class="mt-5" icon-name="cart4" :onClick="goToShop">
          Pide a domicilio
        </default-button>
      </b-jumbotron>
    </section>
    <!--CATEGORIES CAROUSEL-->
    <section class="categories-carousel">
      <b-container>
        <h1 class="text-primary font-weight-bold">Nuestros Productos</h1>
        <hr class="section-hr" />
        <vue-horizontal-list
          :items="brands"
          :options="{
            autoplay: { play: true, repeat: true, speed: 5000 }
          }"
        >
          <template v-slot:default="{ item }">
            <div class="item">
              <b-card
                img-src="../assets/categories/category1.jpeg"
                img-alt="category1"
                :data-label="item.id"
                img-top
                align="center"
                class="shadow rounded"
              >
                <default-button icon-name="cart4" :onClick="goToShop" />
              </b-card>
            </div>
          </template>
        </vue-horizontal-list>
      </b-container>
    </section>
    <!--AD ABOUT DELIVERIES-->
    <section class="delivery-banner">
      <b-container>
        <div class="ad-container shadow rounded">
          <b-img
            :src="require('../assets/delivery-banner.png')"
            center
            fluid
            @click="goToShop()"
            alt="delivery-banner-img"
          ></b-img>
        </div>
      </b-container>
    </section>
    <!--ABOUT US-->
    <section class="about-us">
      <b-container>
        <b-row class="text-left">
          <b-col cols="12" sm="8">
            <h1 class="text-primary font-weight-bold">Sobre nosotros</h1>
            <hr class="section-hr" />
            <p class="lead text-justify">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Et
              commodo semper habitant vestibulum imperdiet donec. Laoreet fames
              in semper habitant. Ut pellentesque quam imperdiet tempus aliquet.
              <br />
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Et
              commodo semper habitant vestibulum imperdiet donec. Laoreet fames
              morbi tellus in semper habitant. Ut pellentesque quam imperdiet
              tempus aliquet
            </p>
            <div class="mx-auto mt-5 text-center">
              <span class="lead font-weight-bold">
                1A Supermarkets
                <span class="text-primary">¡Los Mejores </span>
                <span class="text-secondary">en Todo!</span>
              </span>
            </div>
          </b-col>
          <b-col cols="0" sm="1"></b-col>
          <b-col cols="12" sm="3" class="d-flex align-items-center justify-content-center">
            <b-img
              src="../assets/about-us-img.jpeg"
              center
              fluid
              rounded="circle"
              alt="about-us-img"
            ></b-img>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <!--OUR BRANDS-->
    <section class="our-brands">
      <b-container>
        <h1 class="text-primary font-weight-bold">Nuestros asociados</h1>
        <hr class="section-hr" />
      </b-container>
      <div class="curved-container mt-3 mb-5">
        <b-container class="text-center">
          <b-row align-h="center">
            <b-col cols="8">
              <p class="lead text-white font-weight-bold">
                En 1A Supermarkets contamos con una gran variedad de marcas de
                excelente calidad, siempre siendo ¡los mejores en todo!
              </p>
            </b-col>
          </b-row>
          <b-row align-h="center mt-3">
            <b-col cols="4" sm="3" md="2" lg="1" v-for="brand in brands" :key="brand.id">
              <b-img
                width="80"
                :src="brand.img"
                fluid
                alt="brand-bavaria"
              ></b-img>
            </b-col>
          </b-row>
        </b-container>
      </div>
    </section>
    <!--MAP AND CONTACTS-->
    <section id="map-contact">
      <b-container>
        <h1 class="text-primary font-weight-bold">Donde encontrarnos</h1>
        <hr class="section-hr" />
        <div class="shadow rounded">
          <div class="row">
            <b-col cols="12" sm="5">
              <b-container class="mt-3">
                <h5 class="font-weight-bold">Nuestras sedes</h5>
                <ul class="list-unstyled">
                  <li>
                    <b-icon icon="geo-alt-fill"></b-icon>
                    Calle 48 Bis #92-21
                  </li>
                </ul>
                <h5 class="font-weight-bold">Horarios de Atención</h5>
                <ul class="list-unstyled">
                  <li>
                    Lunes-viernes: 8am a 6pm
                  </li>
                  <li>
                    fin de semana y festivos: 8am a 4pm
                  </li>
                </ul>
                <h5 class="font-weight-bold">Contactos</h5>
                <ul class="list-unstyled">
                  <li>
                    <b-icon icon="chat-dots" />
                    <a href="tel:+573233442359">
                      323 344-2359
                    </a>
                  </li>
                  <li>
                    <b-icon icon="chat-dots" />
                    <a href="tel:+573152611795">
                      315 261-1795
                    </a>
                  </li>
                </ul>
                <h5 class="font-weight-bold">Redes sociales</h5>
                <ul class="list-inline">
                  <li class="list-inline-item">Facebook</li>
                  <li class="list-inline-item">Twitter</li>
                </ul>
              </b-container>
            </b-col>
            <b-col cols="12" sm="7">
              <div>
                <b-embed
                  type="iframe"
                  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d7739.010197748498!2d-76.52063609717749!3d3.3769983217596113!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8e30a110436afcb7%3A0xd020dc8766488ff5!2sCl%2048%20Bis%20%2392-21%2C%20Cali%2C%20Valle%20del%20Cauca%2C%20Colombia!5e0!3m2!1sen!2sru!4v1604029240259!5m2!1sen!2sru"
                  allowfullscreen
                  aria-hidden="false"
                ></b-embed>
              </div>
            </b-col>
          </div>
        </div>
      </b-container>
    </section>
  </main>
</template>

<script>
import DefaultButton from "@/components/DefaultButton";
import VueHorizontalList from "vue-horizontal-list";
export default {
  name: "Home",
  components: { DefaultButton, VueHorizontalList },
  methods: {
    goToShop() {
      this.$router.push({ name: "Shop" });
    }
  },
  data() {
    return {
      brands: [
        { id: 1, img: require("../assets/brands/bavaria.png") },
        { id: 2, img: require("../assets/brands/bavaria.png") },
        { id: 3, img: require("../assets/brands/bavaria.png") },
        { id: 4, img: require("../assets/brands/bavaria.png") },
        { id: 5, img: require("../assets/brands/bavaria.png") },
        { id: 6, img: require("../assets/brands/bavaria.png") },
        { id: 7, img: require("../assets/brands/bavaria.png") },
        { id: 8, img: require("../assets/brands/bavaria.png") }
      ]
    };
  }
};
</script>
<style lang="scss" scoped>
.text-primary {
  color: $primary !important;
}
.text-secondary {
  color: $secondary !important;
}
hr.section-hr {
  background: $secondary;
  height: 5px;
  width: 105px;
  margin-right: 100%;
  margin-bottom: 40px;
}

.jumbotron {
  color: white;
  background-image: url("../assets/landing-hero-bg.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 60vh;
  h1 {
    font-weight: bold;
  }
  & > .container > h1,
  & > .container > p {
    max-width: 60%;
  }
}

@media screen and (max-width: 425px) {
  .jumbotron {
    & > .container > h1,
    & > .container > p {
      max-width: 100%;
    }
  }
}

@media screen and (max-width: 768px) {
  .jumbotron h1 {
    font-size: 2.5rem;
  }
}

section:not(:first-child) {
  margin-top: 130px;
}

section.about-us {
  background: $secondary-section-bg;
  padding: 100px 0;
}

section.delivery-banner {
  img {
    -webkit-transform: scale(1);
    transform: scale(1);
    -webkit-transition: 0.3s ease-in-out;
    transition: 0.3s ease-in-out;
  }
  .ad-container {
    margin: 0;
    padding: 0;
    background: #fff;
    overflow: hidden;
    &:hover img {
      cursor: pointer;
      -webkit-transform: scale(1.1);
      transform: scale(1.1);
    }
  }
}

section.our-brands {
  .curved-container {
    background: $secondary;
    border-bottom-left-radius: 50%;
    border-bottom-right-radius: 50%;
    padding: 55px 0 110px 0;
  }
}
</style>
