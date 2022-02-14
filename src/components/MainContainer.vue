<template>
  <div class="container">
    <movie-box v-for="movie in movies" :key="movie.id" :movie="movie" />
  </div>
</template>

<script>
import MovieBox from "./MovieBox.vue";

export default {
  components: {
    MovieBox,
  },
  props: {
    movies: Array,
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-wrap: wrap;
}
</style>