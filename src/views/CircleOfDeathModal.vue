<template>
  <div class="cd-modal" id="circleOfDeath">
    <div class="modal-content">
      <Card/>
    </div>
  
    <a href="#0" class="modal-close">Close</a>
  </div>
</template>

<script>
import Card from '@/components/Card.vue';

export default {
  name:"circle-of-death-modal",
  components :{
    Card
  }
}
</script>


<style>
  .cd-modal {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 3;
    height: 100%;
    width: 100%;
    overflow: hidden;
    opacity: 0;
    visibility: hidden;
    background-color: #ef8692;
    -webkit-transition: opacity .3s 0s, visibility 0s .3s;
    transition: opacity .3s 0s, visibility 0s .3s;
  }
  
  .cd-modal .modal-content {
    height: 100%;
    overflow-y: auto;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .cd-modal h1,
  .cd-modal h2 {
    text-align: center;
  }
  
  .cd-modal p {
    line-height: 1.6;
    margin: 2em auto;
    max-width: 800px;
  }
  
  .cd-modal .modal-close {
    /* 'X' icon */
    position: absolute;
    z-index: 1;
    top: 20px;
    right: 5%;
    height: 45px;
    width: 45px;
    border-radius: 50%;
    overflow: hidden;
    white-space: nowrap;
    text-indent: 100%;
    color: transparent;
    visibility: hidden;
    opacity: 0;
    -webkit-transform: scale(0);
    transform: scale(0);
    -webkit-transition: visibility 0s .3s, opacity .3s 0s, -webkit-transform .3s 0s;
    transition: visibility 0s .3s, opacity .3s 0s, -webkit-transform .3s 0s;
    transition: transform .3s 0s, visibility 0s .3s, opacity .3s 0s;
    transition: transform .3s 0s, visibility 0s .3s, opacity .3s 0s, -webkit-transform .3s 0s;
  }
  
  .cd-modal .modal-close::before,
  .cd-modal .modal-close::after {
    content: '';
    display: inline-block;
    position: absolute;
    height: 2px;
    width: 20px;
    top: calc(50% - 1px);
    left: calc(50% - 10px);
  }
  
  .cd-modal .modal-close::before {
    -webkit-transform: rotate(45deg);
    transform: rotate(45deg);
  }
  
  .cd-modal .modal-close::after {
    -webkit-transform: rotate(-45deg);
    transform: rotate(-45deg);
  }
  
  .cd-modal.visible {
    opacity: 1;
    visibility: visible;
    -webkit-transition: opacity .7s, visibility 0s;
    transition: opacity .7s, visibility 0s;
  }
  
  .cd-modal.visible .modal-content {
    /* this fixes the buggy scrolling on webkit browsers - mobile devices only - when overflow property is applied */
    -webkit-overflow-scrolling: touch;
  }
  
  .cd-modal.visible .modal-close {
    visibility: visible;
    opacity: 1;
    -webkit-transition: visibility 0s 0s, opacity .3s 0s, -webkit-transform .3s 0s;
    transition: visibility 0s 0s, opacity .3s 0s, -webkit-transform .3s 0s;
    transition: transform .3s 0s, visibility 0s 0s, opacity .3s 0s;
    transition: transform .3s 0s, visibility 0s 0s, opacity .3s 0s, -webkit-transform .3s 0s;
    -webkit-transform: scale(1);
    transform: scale(1);
  }
  
  @media only screen and (min-width: 1100px) {
    .cd-modal .modal-content {
      padding: 6em 5%;
    }
    .cd-modal .modal-close {
      height: 60px;
      width: 60px;
    }
    .cd-modal .modal-close::before,
    .cd-modal .modal-close::after {
      height: 2px;
      width: 26px;
      top: calc(50% - 1px);
      left: calc(50% - 13px);
    }
    .cd-modal p {
      font-size: 2rem;
    }
  }
</style>

