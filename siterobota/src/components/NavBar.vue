<script setup>
</script>

<template>
    <div id="main-container">
        <div id = "header">
            <div id="nav-logo">
                <a href=""><img src="../assets/robota_logo.svg"></a>
                <h1><a href="">Robota</a></h1>
            </div>
            <nav>
                <div id="nav-elements">
                    <ul>
                        <li><a href="">Início</a></li>
                        <li><a href="">Sobre nós</a></li>
                        <li><a href="">Equipes</a></li>
                        <li><a href="">Serviços</a></li>
                        <li><a href="">Contato</a></li>
                    </ul>
                </div>            
                <div id="nav-redes-sociais">
                    <a href=""><img src="../assets/icons8-instagram.svg"></a>
                    <a href=""><img src="../assets/icons8-facebook.svg"></a>
                    <a href=""><img src="../assets/icons8-tiktok.svg"></a>
                    <a href=""><img src="../assets/icons8-twitter.svg"></a>
                </div>
            </nav>
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
    border-bottom: solid black 1px;
    #header {
        a {
        text-decoration: none;
        color: inherit;
        }
        a:hover {
            background-clip: text;
            background-image: linear-gradient(to right, purple , orange);
            color: transparent;
        }
        display: flex;
        justify-content: space-between;
        align-items: center;
        
        #nav-logo {
            display: flex;
            align-items: center;
            h1 {
                font-size: 32px;
                font-weight: 700;
            }
            img {
                width: 64px;
                height: 64px;
            }
        
        }
    
        
        nav {
            display: flex;
            ul {
                list-style: none;
                display: flex;
                gap: 12px;
                li {
                    
                    font-size: 16px;
                    font-weight: 400;
                    color:#252741;
                }
            }
            #nav-redes-sociais {
            display: grid;
            grid-column-gap: 0px;
            grid-template-columns: 23px 23px;
            grid-template-rows: 23px 23px;
            align-self: center;
            margin-left: 24px;
                img {
                    width: 24px;
                    height: 24px;
                }
            }
        }
    }
}    


#menu {
    display:block;
}

</style>
