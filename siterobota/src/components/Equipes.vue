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
                    <p>Fusce vel leo id leo placerat finibus a ac magna. Nullam vitae ipsum dictum, placerat enim eu, mattis turpis. Phasellus convallis felis ac ultricies facilisis. Integer tristique nibh id odio porttitor sollicitudin in nec massa. </p>
                </div>
            </div>
            <div class="equipe">
                <h1>Combate</h1>
                <div class="description">
                    <img>
                    <p>Fusce vel leo id leo placerat finibus a ac magna. Nullam vitae ipsum dictum, placerat enim eu, mattis turpis. Phasellus convallis felis ac ultricies facilisis. Integer tristique nibh id odio porttitor sollicitudin in nec massa. </p>
                </div>
            </div>
            <div class="equipe">
                <h1>Segue-Linha</h1>
                <div class="description">
                    <img>
                    <p>Fusce vel leo id leo placerat finibus a ac magna. Nullam vitae ipsum dictum, placerat enim eu, mattis turpis. Phasellus convallis felis ac ultricies facilisis. Integer tristique nibh id odio porttitor sollicitudin in nec massa. </p>
                </div>
            </div>
        </div>

    </div>

</template>

<style scoped>
    #main-container {
        background-color: #FCF7FF;
        margin-left: 256px;
        margin-right: 256px;
        text-align: center;
        #equipes {
            display: flex;
            justify-content: space-between;
            .equipe {
                border: 2px solid black;

                .description {
                    border: solid 1px black;
                }
            }


        }
    }
</style>
