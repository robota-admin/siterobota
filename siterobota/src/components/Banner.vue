<script setup>
</script>

<template>
    <div id="main-container">
        <div id="banner">
            <div id="heading-container">
                <div id="text-container">
                <h2>EQUIPE DE COMPETIÇÃO DE ROBÓTICA MÓVEL</h2>
                <h3>CTC/DAS/UFSC</h3>
            </div>
            <div id="button-containers">
                <button><h4>PARTICIPAR</h4></button>
                <button><h4>APOIAR</h4></button>
            </div>
            </div>
            
        </div>
    </div>

</template>

<style scoped>
    @media screen and (max-width: 1200px) {
    }
    #main-container {
        width: 100%;
        background-color: grey;
        #banner {
            overflow: hidden;
            height: 64vh;
            background-color:rgba(0, 0, 0, 0.5);
            background: url("src/assets/banner_robota.JPG") no-repeat center center / cover ;
        }
        #heading-container {
            position: relative;
            top: 40%;
            margin-left: 256px;
        }
        #button-containers {
            text-align: center;
            display: flex;
            justify-content: left;
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
        h2 {
            color: white;     
            display: flex;
            font-size: 24px;
        }
        h3 {
            color: white;     
            display: flex;
            font-size: 24px;
        }
    }
    
</style>
