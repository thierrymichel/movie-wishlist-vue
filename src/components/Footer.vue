<template>
  <footer class="site__footer footer">
    <img class="footer__logo" src="/assets/logo-tmdb.svg" />
    <p class="footer__mention">
      This product uses the TMDb API but is not endorsed or certified by TMDb.
    </p>
  </footer>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/utils";
footer {
  display: flex;
  align-items: center;
  padding: 1rem 2rem;
}

img {
  margin-right: 2rem;
  height: 100%;
}
</style>
