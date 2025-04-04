<script setup>
</script>

<template>
<body>
    <h2>QUEM SOMOS</h2>
    <div>
    <p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Vestibulum nec velit id velit efficitur ullamcorper. 
Quisque imperdiet gravida tempus. Duis lacinia quis justo eget porttitor. 
Donec a convallis mi. Donec convallis blandit nibh. Phasellus commodo eros in velit pharetra, sit amet fermentum leo fringilla. Donec auctor eu leo et fermentum. Proin ultrices euismod nulla vel interdum. Fusce ac nisi dolor. Aliquam erat volutpat. Proin sed lorem rutrum, vestibulum nisl vitae, dapibus arcu. Suspendisse at turpis nibh. Nam imperdiet metus urna, nec pharetra libero facilisis id. Morbi sagittis enim sed erat viverra, vel suscipit sapien dictum. 
In eu ipsum et ipsum bibendum accumsan in ut neque.
 Cras vehicula felis sapien, ut facilisis lacus pulvinar nec. </p>
        <div id="info">
            <ul>
                <li><img/><h4>Lorem ipsum dolor sit amet</h4></li>
                <li><img /><h4>Lorem ipsum dolor sit amet</h4></li>
                <li><img /><h4>Lorem ipsum dolor sit amet</h4></li>
                <li><img/><h4>Lorem ipsum dolor sit amet</h4></li>
                <li><img/><h4>Lorem ipsum dolor sit amet</h4></li>
            </ul>
            
        </div>
</div>



</body>

</template>

<style scoped>
body {
    display: grid;
    place-items: center;

    div {
        display:flex;

        p {
            font-size: 12px;
            text-wrap: balanced;
            width: 500px;
        }
    }

    #info {

        ul {
            list-style: none;
            display: flex;
            flex-direction: column;
            margin: 0;
        }
        
        h4 {
            font-size: 12px;
            margin: 0;
        }
    }
}   

</style>
