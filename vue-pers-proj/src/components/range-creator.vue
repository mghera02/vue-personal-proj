<template>
    <input type="range" @change="passRadius" v-model="radius">
</template>

<script>
    export default {
        name: 'rangeCreator',
        data() {
            return {
                radius: 0
            }
        },
        methods: {
            passRadius() {
                this.$emit('passRadius', this.radius);
            }
        }
    }
</script>

<style scoped>
    
</style>