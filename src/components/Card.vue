<template>
    <div id="card">
        <div class="icons">
            <img src="../../public/img/d.png"/>
            <img src="../../public/img/d.png"/>
        </div>
        <h1>K</h1>
         <div class="icons">
            <img src="../../public/img/d.png"/>
            <img src="../../public/img/d.png"/>
        </div>
    </div>
</template>

<script>
    export default {
        name: "card"
    };
</script>

<style>
    @media (max-width: 1025px) {
        #card {
            height: calc(400px * 1.4) !important;
            width: 400px !important;
        }
    }
    
    @media (max-width: 426px) {
        #card {
            height: calc(300px * 1.4) !important;
            width: 300px !important;
        }

        #card h1 {
            font-size: 7em !important;
        }

        .icons {
            height: 50px !important;
        }

        img {
            width: 50px !important;
            height: 50px !important;
        }
    }
    
    @media (max-width: 376px) {
        #card {
            height: calc(250px * 1.4) !important;
            width: 250px !important;
        }
    }
    
    #card {
        background: #f5f5f5;
        height: calc(500px * 1.4);
        width: 500px;
        box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
        border-radius: 5px;
        padding: 5px;
        display: flex;
        justify-content: space-between;
        flex-direction: column;
    }

    img {
        height: 75px;
        width: 75px;
    }

    #card h1 {
        font-family: "Montserrat", sans-serif;
        color: #000000;
        font-size: 10em;
        margin : 0;
    }

    .icons {
        display: flex;
        justify-content: space-between;
        height: 75px;
    }
</style>

