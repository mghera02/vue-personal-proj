<template>
    <input @change="passColor" v-model="rVal">, <input @change="passColor" v-model="gVal">, <input @change="passColor" v-model="bVal"> <input @change="passColor" v-if="isOpaque" v-model="oVal">
</template>

<script>
    export default {
        name: 'colorCreator',
        data() {
            return {
                rVal: 0,
                gVal: 0,
                bVal: 0,
                oVal: 1,
            }
        },
        methods: {
            passColor() {
                this.$emit('passColor', [this.rVal, this.gVal, this.bVal, this.oVal]);
            }
        },
        props: {
            isOpaque: Boolean
        }
    }
</script>

<style scoped>
    input {
        width: 40px;
    }
</style>