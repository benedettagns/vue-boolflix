<template>
    <header>
        <h1>BOOLFLIX</h1>
        <search-box/>
    </header>
</template>

<script>
import SearchBox from './SearchBox.vue'

export default {
    components: { 
        SearchBox 
    },
    
}
</script>

<style lang="scss" scoped>
header {
    color: red;
    background-color: black;
    height: 80px;
}
</style>