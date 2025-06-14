<script setup>
</script>

<template>
    <div id="main-container">
        <h2>NOSSAS EQUIPES</h2>
        <div id="equipes">
            <div class="equipe">
                <h1>Trekking</h1>
                <div class="description">
                    <img src="../assets/trekking.JPG">
                    <p>Robô móvel adaptado para situações de Off-road e On-road, que é capaz de realizar um circuito desconhecido e com obstáculos de maneira completamente autônoma.
                        Seu funcionamento combina princípios de mecânica, eletrônica, programação e modelagem 3D.
                    </p>
                </div>
            </div>
            <div class="equipe">
                <h1>Combate</h1>
                <div class="description">
                    <img src="../assets/combate.JPG">
                    <p>O combate é a principal categoria em competições de robótica,
                         os robôs são separados por peso e controlados por infravermelho. 
                         Seu funcionamento combina princípios de mecânica, eletrônica e modelagem 3D.</p>
                </div>
            </div>
            <div class="equipe">
                <h1>Segue-Linha</h1>
                <div class="description">
                    <img src="../assets/segue_linha.JPG">
                    <p>Robô autônomo projetado para seguir um caminho pré-determinado, geralmente marcado por uma linha no chão, branca ou preta.
                        Seu funcionamento combina princípios de mecânica, eletrônica e programação.</p>
                </div>
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
        text-align: center;
        #equipes {
            display: flex;
            gap: 8px;
            .equipe {
                flex: 1 1 0px;
                border: 1px solid black;
                border-radius: 5px;
                h1 {
                    font-size: 24px;
                }
                .description {
                    padding: 16px;
                    border-top: solid 1px black;
                    border-radius: 5px;
                    img {
                        border: solid black 1px;
                        border-radius: 10px;
                        width: 192px;
                        height: 192px;
                    }
                    p {
                    }
                }
            }


        }
    }
</style>
