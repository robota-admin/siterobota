<script setup>
</script>

<template>
    <div id="header">
        <div id="nav-logo">
            <a href=""><img src=""></a>
            <h1>Robota</h1>
        </div>
        <nav>
            <ul>
                <li><a>Início</a></li>
                <li><a>Sobre nós</a></li>
                <li><a>Equipes</a></li>
                <li><a>Serviços</a></li>
                <li><a>Contato</a></li>
            </ul>
        </nav>
        <div id="nav-redes-sociais">
            <a href="">instagram<img src=""></a>
            <a href="">youtube<img src=""></a>
            <a href="">facebook<img src=""></a>
            <a href="">tiktok<img src=""></a>
        </div>
        <div id="menu"></div>
    </div>

</template>

<style scoped>
#header {
    display: flex;
    justify-content: center;

    h1 {
        background-image: linear-gradient(to right, purple , orange);
        color: transparent;
        background-clip: text;
    }
}
nav > ul {
    list-style: none;
    display: flex;
}
#menu {
    display:block;
}

</style>
