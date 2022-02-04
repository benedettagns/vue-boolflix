<template>
  <div>
    <header-container/>
    <search-box @cerca="watchMovie" @search="watchSeries"/>
    <main-container :movies="movies"/>
  </div>
</template>

<script>
import axios from 'axios'
import HeaderContainer from './components/HeaderContainer.vue'
import MainContainer from './components/MainContainer.vue'
import SearchBox from './components/SearchBox.vue'

export default {
  components: { 
    HeaderContainer, 
    SearchBox, 
    MainContainer 
    },

    data() {
      return {
        movies: [],
        series: [],
      }
    },

    methods: {
      watchMovie(titolo) {

        const details = {
          query: titolo,
          api_key: '417f4df441eb2f30f54f1adfb64efccc',
        }

        axios.get(`https://api.themoviedb.org/3/search/movie`, {details}).then((response) => {
          this.movies = response.data.results;
        })
      },

      watchSeries(titolo) {
        const details = {
          query: titolo,
          api_key: '417f4df441eb2f30f54f1adfb64efccc'
        }

        axios.get(`https://api.themoviedb.org/3/search/tv`, {details}).then((response) => {
          this.series = response.data.results
        })
      }
    }
  
}
</script>

<style lang="scss" scoped>

</style>