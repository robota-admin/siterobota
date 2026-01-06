<script setup>
import Banner from './components/Banner.vue';
import NavBar from './components/NavBar.vue'
import QuemSomos from './components/QuemSomos.vue';
import Equipes from './components/Equipes.vue';
import Servicos from './components/Servicos.vue';
import Patrocinadores from './components/Patrocinadores.vue';
import Contato from './components/Contato.vue';
import Footer from './components/Footer.vue';
</script>



<template>
  <header>
  </header>

  <main>
    <NavBar></NavBar>
    <Banner></Banner>
    <QuemSomos></QuemSomos>
    <Equipes></Equipes>
    <Servicos></Servicos>
    <Patrocinadores></Patrocinadores>
    <Contato></Contato>
    <Footer></Footer>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

/* Separadores visuais entre seções */
main > *:not(:last-child) {
  position: relative;
}

main > *:not(:last-child):after {
  content: '';
  position: absolute;
  bottom: -40px;
  left: 50%;
  transform: translateX(-50%);
  width: 100px;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--main-purple), transparent);
  opacity: 0.2;
}

/* Espaçamento específico para seções */
main > * {
  margin-bottom: 40px; /* 80px */
}

main > *:last-child {
  margin-bottom: 0;
}

/* Responsividade */
@media screen and (max-width: 1200px) {
  main > * {
    margin-bottom: 35px; /* 60px */
  }

  main > *:not(:last-child):after {
    bottom: -30px;
    width: 80px;
  }
}

@media screen and (max-width: 768px) {
  main > * {
    margin-bottom: 30px; /* 50px */
  }

  main > *:not(:last-child):after {
    bottom: -25px;
    width: 60px;
    height: 2px;
  }
}

@media screen and (max-width: 480px) {
  main > * {
    margin-bottom: 25px; /* 40px */
  }

  main > *:not(:last-child):after {
    bottom: -20px;
    width: 50px;
    height: 1.5px;
  }
}

@media screen and (max-width: 360px) {
  main > * {
    margin-bottom: 20px;
  }

  main > *:not(:last-child):after {
    width: 40px;
  }
}
</style>
