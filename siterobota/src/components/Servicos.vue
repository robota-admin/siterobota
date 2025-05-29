<script setup>
</script>

<template>
<div id="main-container">
    <h2>SERVIÇOS</h2>
    <div id="servicos">
        <div id="descricao">
            <h3>Também ofertamos os seguintes serviços para membros da graduação e empresas: </h3>
            <ul>
                <li>Impressão 3D</li>
                <li>Modelagem</li>
                <li>Mecânica</li>
                <li>Eletrônica</li>
            </ul>
        </div>
            <div id="images">
                <div id="image"></div>
                <div id="image"></div>
                <div id="image"></div>
                <div id="image"></div>
                <div id="image"></div>
                <div id="image"></div>
        </div>
    </div>
    
    
</div>

</template>

<style scoped>
    #main-container {
        @media screen and (max-width: 1200px) {
            margin-left: 96px;
            margin-right: 96px;
        }
        margin-left: 256px;
        margin-right: 256px;
        #servicos {
            display: flex;


        }
        #descricao {
            h3 {
                font-size: 24px;
                line-clamp: 3;
            }
            li {
                font-size: 24px;
            }
        }
        #images {
            margin: 16px;
            width: 384px;
            flex-shrink: 0;
            flex-grow: 1;
            background-color: aliceblue;
            #image {

            }
        }
    }
</style>