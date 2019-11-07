<template>
  <nav class="site__nav nav">
    <ul class="nav__list">
      <li class="nav__item is-active">
        <a class="nav__item__link" href="/">Home</a>
      </li>
      <li class="nav__item">
        <a class="nav__item__link" href="#">Search</a>
      </li>
      <li class="nav__item">
        <a class="nav__item__link" href="#">Watchlist</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Nav"
};
</script>

<style lang="scss">
@import "../styles/utils";
.nav__item {
  border-bottom: 1px solid $c-darker;
}

.nav__item__link {
  display: block;
  padding: 2rem;
  color: $c-light;
  text-decoration: none;
  transition: background-color 0.35s ease-in-out;

  &:hover {
    background-color: $c-darker;
  }

  .is-active > & {
    background-color: lighten($c-dark, 10%);
    pointer-events: none;
  }
}
</style>
