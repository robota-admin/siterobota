<script setup>
</script>

<template>
    <div id="main-container">
            <img src="../assets/banner_robota.JPG">
            <h2>EQUIPE DE COMPETIÇÃO DE ROBÓTICA MÓVEL</h2>
            <h3>CTC/DAS/UFSC</h3>
        <div id="button-containers">
            <button><h4>PARTICIPAR</h4></button>
            <button><h4>APOIAR</h4></button>
        </div>
    </div>

</template>

<style scoped>
    #main-container {

        position:relative;
        width: 100%;
        background-color: grey;
        #button-containers {
            position: absolute;
            text-align: center;
            left: 256px;
            top: 50%;
            display: flex;
            gap: 8px;
            button {
                border-radius: 12px;
                border: none;
                text-align: center;
            }

            h4 {
                font-weight: 700;
                font-size: 12px;
                width: 96px;
                
            }
        }
        img {
            width: 100%;
            height: 640px;
            opacity: 0.3;
        }
        h2 {
            position: absolute;
            top: 35%;
            left: 256px;
            color: white;     
            display: flex;
            font-size: 24px;
        }
        h3 {

            position: absolute;
            top: 40%;
            left: 256px;
            color: white;     
            display: flex;
            font-size: 24px;
        }
    }
    
</style>
