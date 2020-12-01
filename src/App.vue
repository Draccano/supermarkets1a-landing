<template>
  <div id="app">
    <main-navbar />
    <router-view />
    <main-footer />
  </div>
</template>

<script>
import MainNavbar from "@/components/MainNavbar";
import MainFooter from "@/components/MainFooter";
export default {
  components: { MainFooter, MainNavbar }
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Open+Sans");
#app {
  font-family: "Open Sans", sans-serif;
}
</style>
