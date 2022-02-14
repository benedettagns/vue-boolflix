<template>
  <div>
    <header-container />
    <search-box @cerca="watchMovie" @search="watchSeries" />
    <main-container :movies="movies" />
  </div>
</template>

<script>
import axios from "axios";
import HeaderContainer from "./components/HeaderContainer.vue";
import MainContainer from "./components/MainContainer.vue";
import SearchBox from "./components/SearchBox.vue";

export default {
  components: {
    HeaderContainer,
    SearchBox,
    MainContainer,
  },

  data() {
    return {
      movies: [],
    };
  },
  mounted(){
    this.watchMovie("titanic")
  },

  methods: {
    
    watchMovie(titolo) {
      if (titolo != "") {
        const apiKey = "417f4df441eb2f30f54f1adfb64efccc";
        let strApi =
          "https://api.themoviedb.org/3/search/movie?api_key=" +
          apiKey +
          "&query=" +
          titolo;

        axios.get(strApi).then((response) => {
          this.movies = response.data.results;
        });
      }
    },

    watchSeries(titolo) {
      if (titolo != "") {
        const apiKey = "417f4df441eb2f30f54f1adfb64efccc";
        let strApi =
          "https://api.themoviedb.org/3/search/tv?api_key=" +
          apiKey +
          "&query=" +
          titolo;

        axios.get(strApi).then((response) => {
          this.movies = response.data.results;
        });
      }
    },
  },
};
</script>

<style lang="scss" >
@import 'style/main.scss'
</style>