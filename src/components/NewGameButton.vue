<template>
  <a href="#circleOfDeath" class="cd-btn cd-modal-trigger"> <i class="fas fa-play" /> New Game</a>
</template>

<script>
  export default {
    name: "new-game-button"
  };
</script>

<style scoped>
  @media (max-width: 426px) {
    .cd-btn {
      font-size: 1.2em !important;
      padding: 0.5em 1em;
    }
  }
  
  .cd-btn {
    display: inline-block;
    line-height: 50px;
    padding: 0.5em 1em;
    font-size: 2em;
    border-radius: 50px;
    background-color: #778beb;
    border: none;
    box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
    transition: box-shadow 0.1s cubic-bezier(0.25, 0.8, 0.25, 1);
    color: #f5f5f5;
  }
  
  .cd-btn:hover {
    box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
  }
  
  a {
    text-decoration: none;
  }
</style>
