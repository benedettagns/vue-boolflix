<template>
    <div>
        <input type="text" placeholder="cerca" v-model="titoloCercato">
        <button @click="$emit('cerca', titoloCercato)">Cerca film</button>
        <button @click="$emit('search', titoloCercato)">Cerca serie</button>
    </div>
</template>

<script>
export default {
    data() {
        return{
            titoloCercato: '',
        }  
    }
}
</script>

<style lang="scss" scoped>
input {
    background-color: white;
    margin-left: 10px;
    width: 200px;
}

button {
    background-color: white;
    width: 100px;
    margin-left: 10px;
}
</style>