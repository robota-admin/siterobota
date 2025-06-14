<script setup>
</script>

<template>
<div id="main-container">
    <div id="informacoes">
        <h2>ROBOTA UFSC</h2>
        <p>LTIC - Laboratório de Tecnologia e Comunicação <br>Av. Prof. Henrique da Silva Fontes, 1 - Trindade,<br> Florianópolis - SC, 88036-700</p>
        <h3>Email: robotadasufsc@gmail.com</h3>
        <h3>Whatsapp: (48) 3721-4609</h3>
        <div id="nav-redes-sociais">
            <a href=""><img src="../assets/icons8-instagram.svg"></a>
            <a href=""><img src="../assets/icons8-facebook.svg"></a>
            <a href=""><img src="../assets/icons8-tiktok.svg"></a>
            <a href=""><img src="../assets/icons8-twitter.svg"></a>
        </div>
    </div>
    <div id="localizacao">
        <img src="../assets/mapstest.png">
    </div>
    <div id="patrocinadores">
        <h3>Patrocinadores</h3>
        <div id="images">
            <a href=""><img></a>
            <a href=""><img></a>
            <a href=""><img></a>
            <a href=""><img></a>
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
        display: flex;
        gap:96px;
        #nav-redes-sociais {
            display: flex;
            gap: 12px;
                img {
                    width: 24px;
                    height: 24px;
                }
                a {
                    padding: 8px;
                    background-color: #F4F5F5;
                    border-radius: 8px;
                }
            }
        #informacoes {
            h2 {
                font-size: 24px;
            }
            p {
                font-size: 16px;
            }
            h3 {
                font-size: 16px;
            }
        }
        #localizacao {
            background-color: #F4F5F5;
            width: 384px;
            height: 256px;
            flex: 1 0 256px;
            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }
        #patrocinadores {
        
            text-align: center;

            #images {
           
                display: grid;
                grid-template-columns: 1fr 1fr;
                grid-template-rows: 1fr 1fr;
                img {
                    width: 64px;
                    height: 64px;
                }
            }
        }
        
    }
</style>