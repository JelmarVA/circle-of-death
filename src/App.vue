<template>
  <div id="app">
    <Home/>
    <CircleOfDeathModal/>
    <TransitionLayer/>
  </div>
</template>

<script>
  import TransitionLayer from "@/components/TransitionLayer.vue";
  import Home from "@/views/Home.vue";
  import CircleOfDeathModal from "@/views/CircleOfDeathModal.vue";
  
  export default {
    name: "app",
    components: {
      TransitionLayer,
      Home,
      CircleOfDeathModal
    }
  };
</script>


<style>
  @import "https://fonts.googleapis.com/css?family=Montserrat|Rock+Salt";
  html,
  body {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: "Montserrat", sans-serif;
  }
  
  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    background-color: #1b1464;
    color: #f5f5f5;
    height: 100%;
    width: 100%;
  }
  
  .cd-main-content {
    height: 100%;
  }
</style>
