<template>
    <div>
        <input type="text" placeholder="cerca" v-model="titoloCercato">
        <button>Cerca</button>
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

</style>