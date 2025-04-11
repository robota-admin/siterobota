<script setup>
</script>

<template>
    <div id="header">
        <div id = "main-container">
            <div id="nav-logo">
                <a href=""><img src="../assets/robota_logo.svg"></a>
                <h1>Robota</h1>
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
#header {
    a {
        text-decoration: none;
        color: inherit;
    }
    
    border-bottom: solid black 1px;
    #main-container {
        
        display: flex;

        align-items: center;
        justify-content: space-between;
        
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
                    color:252741;
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
