<template>
  <div class="film-box">

    <div class="card-film">

      <div class="indietro">
        <p> Titolo:{{ movie.title }}</p>
        <p>Titolo originale:{{ movie.original_title }}</p>

        <p> {{ movie.original_language }}</p>

        <p>Voto: <i class="fa-solid fa-star">{{ Math.round(movie.vote_average/2) }} </i></p>
        <p>Trama: {{ movie.overview }}</p>
      </div>

      <div class="davanti">
        <img v-if="movie.poster_path!=null" :src="`https://image.tmdb.org/t/p/w342/${movie.poster_path}`" :alt="movie.poster_path" />
      </div>
      
    </div>
  </div>
</template>

<script>
export default {
  props: {
    movie: Object,
  },
};
</script>

<style lang="scss" scoped>
.film-box {
  width: calc(100% / 6);
  margin: 10px ;

  p {
    color: white;
    padding: 10px;
    font-size: 12px;

    i {
      color: yellow;
    }
  }

  .card-film {
    background-color: black;
    cursor: pointer;
    overflow-y: auto;

    &:hover {
      .indietro {
        display: block;
      }

      .davanti {
        display: none;
      }

    }

    .davanti img {
      width: 100%; 
    }

    .indietro {
      display: none;
    }

    
  }
}
</style>