<template>
    <div class="backgroundColor" id="rhs">
        <div class="containerColor fontColor borderRadius" id="container">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc fermentum augue urna, ut maximus sapien commodo eu. Sed elementum blandit orci. Pellentesque vulputate felis fermentum lacus laoreet, eget dictum urna facilisis. Donec eget semper tortor.
        </div>
        <div class="containerColor fontColor borderRadius" id="container">
            Suspendisse in sapien non felis maximus ornare. Maecenas ultrices egestas semper. Curabitur diam leo, tempor in vestibulum id, sodales fermentum mi. Vestibulum maximus purus risus, sed lacinia augue iaculis sit amet. Quisque venenatis enim dui, et volutpat nunc laoreet a. Ut sodales justo ut arcu vehicula consequat. Aliquam neque metus, venenatis a purus eget, euismod gravida diam.
        </div>
    </div>
</template>

<script>
    export default {
        name: 'viewPanel',
        props: {
            background: String,
            containers: String,
            font: String,
            radius: String,
        }
    }
</script>

<style scoped>
    #rhs {
        position: absolute;
        top: 0vw;
        left:50vw;
        width: 50vw;
        height:100vh;
        margin-top:2vw;
    }
    #container {
        width: 75%;
        margin-top: 30px;
        margin-left: auto;
        margin-right: auto;
        padding: 20px;
        padding-bottom: 5px;
    }
    .backgroundColor{
        background: v-bind('background');
    }
    .containerColor{
        background: v-bind('containers');
    }
    .fontColor {
        color: v-bind('font');
        font-size: 20px;
        font-family: 'Heebo', sans-serif;
    }
    .borderRadius {
        border-radius: calc(v-bind('radius')*1px);
    }
</style>