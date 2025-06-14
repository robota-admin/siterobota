<script setup>
import Banner from './components/Banner.vue';
import NavBar from './components/NavBar.vue'
import QuemSomos from './components/QuemSomos.vue';
import Equipes from './components/Equipes.vue';
import Servicos from './components/Servicos.vue';
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
    <Contato></Contato>
    <Footer></Footer>
  </main>
</template>

<style scoped>
main {
  
  display: flex;
  flex-direction: column;
  gap: 16px;
}

</style>
