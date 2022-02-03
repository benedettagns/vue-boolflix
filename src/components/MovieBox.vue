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

</style>