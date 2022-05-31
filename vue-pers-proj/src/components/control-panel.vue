<template>
    <div id="lhs">
        <colorPicker 
            @passBackground="passBackground"
            @passContainers="passContainers"
            @passFont="passFont"
            @passRadius="passRadius"
            />
    </div>
</template>

<script>
    import colorPicker from './color-picker.vue'

    export default {
        name: 'controlPanel',
        components: {
            colorPicker
        },
        methods: {
            passBackground(color){
                this.$emit('passBackground', color)
            },
            passContainers(color){
                this.$emit('passContainers', color)
            },
            passFont(color){
                this.$emit('passFont', color)
            },
            passRadius(radius){
                this.$emit('passRadius', radius)
            }
        }
    }
</script>

<style scoped>
    #lhs {
        background: rgb(240,240,255);
        width: 50vw;
        height:100vh;
    }
</style>