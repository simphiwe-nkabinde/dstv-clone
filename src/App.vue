<script setup>
import { RouterView } from 'vue-router'
import Header from './components/Header.vue';
import SubNav from './components/SubNav.vue';
import HomeView from './views/HomeView.vue';
</script>

<template>
  <Header></Header>
  <!-- <SubNav></SubNav> -->
  <main>
    <RouterView/>   
  </main>
  
</template>