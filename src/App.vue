<script setup>
import { RouterView } from 'vue-router'
import Header from './components/Header.vue';
import HomeView from './views/HomeView.vue';
</script>

<template>
  <Header></Header>
  <main>
    <RouterView/>   
  </main>
  
</template>