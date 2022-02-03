<template>
  <div>
    <header-container/>
    <search-box @cerca="watchMovie"/>
    <main-container/>
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
      }
    },

    methods: {
      watchMovie(titoloCercato) {
        axios.get('https://api.themoviedb.org/3/search/movie?api_key=417f4df441eb2f30f54f1adfb64efccc&query=' + titoloCercato).then((response) =>{
          this.movies = response.data.results;
        })
      }
    }
  
}
</script>

<style lang="scss" scoped>

</style>