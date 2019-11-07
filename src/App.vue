<template>
  <div id="app" class="site">
    <Nav />
    <main class="site__main">
      <h1>Movie wishlist</h1>
      <ul class="listing"></ul>
    </main>
    <Footer />
  </div>
</template>

<script>
import Footer from "./components/Footer.vue";
import Nav from "./components/Nav.vue";

export default {
  name: "app",
  components: {
    Footer,
    Nav
  }
};
</script>

<style lang="scss">
@import "./styles/utils";
@import "./styles/global";

body > svg {
  display: none;
}
</style>
