<template>
  <div>
    <b-navbar id="global-navbar" toggleable="lg" type="dark" variant="dark">
      <b-container>
        <b-navbar-brand to="/">
          <b-img
            src="../assets/logo-nav.png"
            class="rounded"
            alt="navbar-logo"
            height="40"
          />
        </b-navbar-brand>

        <b-navbar-toggle target="main-nav-collapse"></b-navbar-toggle>

        <b-collapse id="main-nav-collapse" is-nav>
          <!-- center aligned search form -->
          <b-navbar-nav class="mx-auto">
            <b-nav-form>
              <b-input-group size="md">
                <b-input-group-prepend is-text>
                  <b-icon icon="search"></b-icon>
                </b-input-group-prepend>
                <b-form-input
                  type="search"
                  placeholder="Que buscas?"
                ></b-form-input>
              </b-input-group>
            </b-nav-form>
          </b-navbar-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav>
            <b-nav-item href="#">
              <b-icon icon="cart4"></b-icon>
            </b-nav-item>
            <b-nav-item href="#">
              <b-icon icon="box-seam"></b-icon>
            </b-nav-item>
            <b-nav-item to="/login">
              <b-icon icon="person-circle"></b-icon>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
    <!--NAVEGARTION NAVBAR-->
    <b-navbar id="navigation-navbar" toggleable="lg">
      <b-container>
        <b-navbar-toggle target="navigation-nav-collapse"></b-navbar-toggle>

        <b-collapse id="navigation-nav-collapse" is-nav>
          <b-navbar-nav class="mx-auto">
            <b-nav-item to="/">Inicio</b-nav-item>
            <b-nav-item to="/shop">Tienda</b-nav-item>
            <!--<b-nav-item to="/categories">Productos</b-nav-item>-->
            <b-nav-item to="/#map-contact">Contáctenos</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "MainNavbar",
  components: {}
};
</script>
<style lang="scss" scoped>
nav#global-navbar {
  background: $primary !important;
  height: 75px;
  a.nav-link {
    font-size: 1.4rem;
  }
}

nav#navigation-navbar {
  background: $secondary-navbar-bg !important;
  height: 50px;
  a {
    color: $navbar-text;
    &:hover {
      text-decoration: none;
    }
    &.router-link-exact-active {
      color: $secondary;
      font-weight: bold;
    }
  }
}
</style>
