<script setup>
import Banner from './components/Banner.vue';
import NavBar from './components/NavBar.vue'
import QuemSomos from './components/QuemSomos.vue';
</script>



<template>
  <header>
  </header>

  <main>
    <NavBar></NavBar>
    <Banner></Banner>
    <QuemSomos></QuemSomos>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  gap: 48px;
}

</style>
