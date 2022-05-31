<template>
    <h1> Choose Colors </h1>
    <h3> Background: <colorCreator @passColor="passBackground" :isOpaque='false' /></h3>
    <h3> Containers: <colorCreator @passColor="passContainers" :isOpaque='true' /></h3>
    <h3> Font Color: <colorCreator @passColor="passFont" :isOpaque='false' /></h3>
    <h1> Choose other Settings</h1>
    <h3> Border Radius: <rangeCreator @passRadius="passRadius" /></h3>
</template>

<script>
    import colorCreator from './color-creator.vue'
    import rangeCreator from './range-creator.vue'

    export default {
        name: 'colorPicker',
        components: {
            colorCreator,
            rangeCreator,
        },
        methods: {
            passBackground(color){
                this.$emit('passBackground', `rgb(${color[0]}, ${color[1]}, ${color[2]})`)
            },
            passContainers(color){
                this.$emit('passContainers', `rgba(${color[0]}, ${color[1]}, ${color[2]}, ${color[3]})`)
            },
            passFont(color){
                this.$emit('passFont', `rgb(${color[0]}, ${color[1]}, ${color[2]})`)
            },
            passRadius(radius){
                this.$emit('passRadius', radius);
            }
        }
    }
</script>

<style scoped>
    h1 {
        font-size: 30px;
        margin-top: 0px;
        padding-top: 5px;
        font-family: 'Heebo', sans-serif;
        text-align: center;
        color: rgb(40,40,40);
    }
    h3 {
        font-size: 20px;
        margin-top: 0px;
        padding-top: 5px;
        padding-left: 5px;
        font-family: 'Heebo', sans-serif;
        color: rgb(50,50,50);
    }

</style>