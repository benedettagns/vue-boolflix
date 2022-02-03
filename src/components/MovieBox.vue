<template>
    <div class="film-box">
        <p>{{movie.title}}</p>
        <p> {{movie.original_title}} </p>
        <p> {{movie.vote_average}} </p>
        <p> {{movie.overview}} </p>
    </div>
</template>

<script>

export default {
    props: {
        film: Object,
    }
}
</script>

<style lang="scss" scoped>
.film-box {
    width: 100px;
    height: 100px;
    background-color: grey;
    border: 1px solid;
}
</style>