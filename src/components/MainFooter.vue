<template>
  <footer>
    <b-container>
      <b-row>
        <b-col>
          <h5 class="font-weight-bold">Nosotros</h5>
          <ul class="list-unstyled">
            <li>Todo sobre 1A</li>
            <li>Nuestros asociados</li>
            <li>Pruductos</li>
            <li>Mas información</li>
          </ul>
        </b-col>
        <b-col>
          <h5 class="font-weight-bold">Información</h5>
          <ul class="list-unstyled">
            <li>Politicas de envío y devolución</li>
            <li>Política de privacidad</li>
            <li>Términos y condiciones</li>
          </ul>
        </b-col>
        <b-col>
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
        </b-col>
        <b-col>
          <h5 class="font-weight-bold">Nuestras sedes</h5>
          <ul class="list-unstyled">
            <li>
              <b-icon icon="geo-alt-fill"></b-icon>
              Calle 48 Bis #92-21
            </li>
          </ul>
        </b-col>
        <b-col class="d-flex align-items-center justify-content-center">
          <b-img
            src="../assets/logo-footer.png"
            center
            fluid
            alt="about-us-img"
          ></b-img>
        </b-col>
      </b-row>
    </b-container>
  </footer>
</template>

<script>
export default {
  name: "MainFooter",
  components: {}
};
</script>
<style lang="scss" scoped>
footer {
  color: white;
  background: $primary;
  margin-top: 120px;
  padding: 75px 0 85px 0;
  h5 {
    margin-bottom: 15px;
  }
  ul li {
    margin-bottom: 6px;
    a {
      color: white;
      &:hover {
        text-decoration: none;
        color: darken(white, 20);
      }
    }
  }
}
</style>
