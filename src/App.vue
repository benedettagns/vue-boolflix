<template>
  <div>
    <header-container/>
    <search-box />
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
  
}
</script>

<style lang="scss" scoped>

</style>