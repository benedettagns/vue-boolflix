<template>
  <div id="app">
    <header-container/>
    <main-container/>
  </div>
</template>

<script>
import axios from 'axios'
import HeaderContainer from './components/HeaderContainer.vue'
import MainContainer from './components/MainContainer.vue'

export default {
  name: 'App',
  components: {
    HeaderContainer , 
    MainContainer,
  },

  data() {
    return{
      movies: [],
    } 
  },

  mounted() {
    axios.get('https://api.themoviedb.org/3/search/movie?api_key=417f4df441eb2f30f54f1adfb64efccc&query=(bisogna aggiungere qualcosa)').then((response) => {
      this.movies = response.data.results;
      
    })
  },

  
}
</script>

<style lang="scss">

</style>
