<script setup>
</script>

<template>
    <div id="main-container">
        <h2>NOSSAS EQUIPES</h2>
        <div id="equipes">
            <div class="equipe">
                <h1>Trekking</h1>
                <div class="description">
                    <img>
                    <p>Robô móvel, que é capaz de realizar um circuito, desconhecido e com obstáculos, de maneira completamente autônoma.</p>
                </div>
            </div>
            <div class="equipe">
                <h1>Combate</h1>
                <div class="description">
                    <img>
                    <p>o combate é uma categoria bem popular em competições de robótica, os robôs são separados em categorias de peso e organizados em chaves de combates 1 a 1 em que o vencedor passa para a próxima luta</p>
                </div>
            </div>
            <div class="equipe">
                <h1>Segue-Linha</h1>
                <div class="description">
                    <img>
                    <p>Um seguidor de linha é um robô autônomo projetado para seguir um caminho pré-determinado, geralmente marcado por uma linha no chão, branca ou preta.
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
            justify-content: space-between;
            .equipe {
                width: 256px;
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
