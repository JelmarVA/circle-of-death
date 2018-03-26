<template>
  <div class="home">
    <h1>Circle of Death</h1>
    <NewGameButton/>
  </div>
</template>

<script>
  import NewGameButton from '@/components/NewGameButton.vue';
  
  export default {
    name: 'home',
    components: {
      NewGameButton
    }
  }
</script>

<style>
  @media (max-width: 426px) {
    h1 {
      font-size: 3em !important;
    }
  }
  
  h1 {
    font-size: 5em;
    font-family: 'Rock Salt', cursive;
  }
  
  .home {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
  }
  
  .cd-main-content {
    position: relative;
    z-index: 1;
    width: 100%;
    height: 100vh;
    /* vertically align its content */
    display: table;
  }
  
  .cd-main-content .center {
    /* vertically align inside parent element */
    display: table-cell;
    vertical-align: middle;
    text-align: center;
  }
</style>

