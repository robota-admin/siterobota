<script setup>
</script>

<template>
    <div id="main-container">
        <h2>QUEM SOMOS</h2>
        <div id="descricao">
        <p>

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
    Vestibulum nec velit id velit efficitur ullamcorper. 
    Quisque imperdiet gravida tempus. Duis lacinia quis justo eget porttitor. 
    Donec a convallis mi. Donec convallis blandit nibh. Phasellus commodo eros in velit pharetra, sit amet fermentum leo fringilla. Donec auctor eu leo et fermentum. Proin ultrices euismod nulla vel interdum. Fusce ac nisi dolor. Aliquam erat volutpat. Proin sed lorem rutrum, vestibulum nisl vitae, dapibus arcu. Suspendisse at turpis nibh. Nam imperdiet metus urna, nec pharetra libero facilisis id. Morbi sagittis enim sed erat viverra, vel suscipit sapien dictum. 
    In eu ipsum et ipsum bibendum accumsan in ut neque.
    Cras vehicula felis sapien, ut facilisis lacus pulvinar nec. </p>
            <div id="info">
                <ul>
                    <li><img/><h4>20+ anos de existência.</h4></li>
                    <li><img /><h4>30+ membros.</h4></li>
                    <li><img /><h4>7+ robôs desenvolvidos.</h4></li>
                    <li><img/><h4>7+ competições disputadas</h4></li>
                </ul>
                
            </div>
        </div>
    </div>





</template>

<style scoped>
    #main-container {
        @media screen and (max-width: 1200px) {
            margin-left: 168px;
            margin-right: 168px;
        }
        margin-left: 256px;
        margin-right: 256px;
        h2 {
            text-align: center;
        }

    }
    #descricao {
        display:flex;
        p {
            font-size: 16px;
            text-wrap: n;
        }
    }

    #info {

        ul {
            list-style: none;
            display: flex;
            flex-direction: column;
            padding: 0;
            margin: 0;
        }
        
        h4 {
            font-size: 24px;
            font-weight: 1000;
            margin: 0;
            text-wrap: balanced;
        }
    }
   

</style>
