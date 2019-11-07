<template>
  <div id="app" class="site">
    <Nav />
    <main class="site__main">
      <h1>Movie wishlist</h1>
      <Listing />
    </main>
    <Footer />
  </div>
</template>

<script>
import Footer from "./components/Footer.vue";
import Listing from "./components/Listing.vue";
import Nav from "./components/Nav.vue";

export default {
  name: "app",
  components: {
    Footer,
    Listing,
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
