<template>
    <div class="container">
        <movie-box v-for="movie in movies" :key="movie.id" :movies="movies"/>
    </div>
</template>

<script>
import MovieBox from './MovieBox.vue'

export default {
    components: { 
        MovieBox 
    },
    props: {
        films: Array,
    }
}
</script>

<style lang="scss" scoped>
.container{
    height: 500px;
    background-color: whitesmoke;
}
</style>