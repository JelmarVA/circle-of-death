<template>
    <div class="cd-transition-layer" data-frame="25">
        <div class="bg-layer"></div>
    </div>
</template>

<script>
    export default {
        name: "transition-layer"
    }
</script>

<style>
    .cd-transition-layer {
        position: fixed;
        top: 0;
        left: 0;
        z-index: 2;
        height: 100%;
        width: 100%;
        opacity: 0;
        visibility: hidden;
        overflow: hidden;
    }
    
    .cd-transition-layer .bg-layer {
        position: absolute;
        left: 50%;
        top: 50%;
        -webkit-transform: translateY(-50%) translateX(-2%);
        transform: translateY(-50%) translateX(-2%);
        /* its dimentions will be overwritten using jQuery to proportionally fit the viewport */
        height: 100%;
        background-size: 100% 100%;
        background-repeat: no-repeat;
        background-position: 0 0;
    }
    
    .cd-transition-layer.visible {
        opacity: 1;
        visibility: visible;
    }
    
    .cd-transition-layer.visible .bg-layer {
        -webkit-transform: translateY(-50%) translateX(-98%);
        transform: translateY(-50%) translateX(-98%);
    }
    
    .cd-transition-layer.opening .bg-layer,
    .cd-transition-layer.closing .bg-layer {
        -webkit-animation-duration: .8s;
        animation-duration: .8s;
        -webkit-animation-fill-mode: forwards;
        animation-fill-mode: forwards;
    }
    
    .no-cssanimations .cd-transition-layer {
        display: none;
    }
</style>


