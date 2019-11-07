<template>
  <ul>
    <li class="item"
      v-for="m in movies"
      :key="m.id">
      {{ m.title }}
    </li>
  </ul>
</template>

<script>
import movies from '../data/movies.json';

export default {
  name: "Listing",
  data() {
    return {
      movies: movies.results,
      title: 'Mon titre',
      inc: 0,
    };
  },
  mounted() {
    // setInterval(() => {
    //   this.inc++;
    // }, 500);
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/utils";
.listing,
[class*="listing--"] {
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 2rem;
  grid-auto-rows: 24rem;

  @include mq(l) {
    grid-template-columns: repeat(2, 1fr);
  }

  @include mq(xl) {
    grid-template-columns: repeat(3, 1fr);
  }

  @include mq(xxl) {
    grid-template-columns: repeat(4, 1fr);
  }
}

.item,
[class*="item--"] {
  position: relative;
  display: flex;
  flex-direction: column-reverse;
  overflow: hidden;
}

.item__title {
  position: relative;
  z-index: 2;
  padding: 1rem 1.5rem;
  background-image: linear-gradient(to top, $c-black 0%, rgba($c-black, 0.35));
  font-size: 2rem;
  line-height: 1.1;
  will-change: transform;

  > * {
    will-change: transform, opacity;
  }
}

.item__poster {
  position: absolute;
  z-index: 1;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  will-change: opacity;
}

.item__like {
  position: absolute;
  z-index: 2;
  right: 1rem;
  bottom: 1rem;
}

.like,
[class*="like--"] {
  border: 0;
  padding: 0;
  background: none;
  fill: $c-white;
  opacity: 0.65;
  transition: fill 0.25s ease-in-out, opacity 0.25s ease-in-out;
  cursor: pointer;

  &:hover,
  &:focus {
    outline: 0;
    opacity: 1;
  }

  &.is-selected {
    opacity: 1;
    fill: $c-pink;
  }

  svg {
    display: block;
    width: 2.4rem;
    height: 2.4rem;
    fill: inherit;
  }
}
</style>
