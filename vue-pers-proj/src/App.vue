<template>
  <controlPanel
    @passBackground="getBackground"
    @passContainers="getContainers"
    @passFont="getFont"
    @passRadius="getRadius"
    />
  <viewPanel 
    :background='background' 
    :containers='containers' 
    :font='font'
    :radius='radius'
    />
</template>

<script>
  import controlPanel from './components/control-panel.vue'
  import viewPanel from './components/view-panel.vue'

  export default {
    name: 'App',
    components: {
      controlPanel,
      viewPanel
    },
    data() {
      return {
        background: '',
        containers: '',
        font: '',
        radius: '',
      }
    },
    methods: {
      getBackground(color){
        this.background = color;    
      },
      getContainers(color){
        this.containers = color;  
      },
      getFont(color){
        this.font = color;  
      },
      getRadius(radius){
        this.radius = String(radius);  
        console.log(radius)
      }
    }
  }
</script>

<style>
  html {
    height: 100vh;
    width: 50vw;
    overflow: hidden;
    margin: 2vw;
  }
  body {
    margin: 0;
  }
  #App {
  }
</style>
