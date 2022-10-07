<script setup>
import { RouterView } from 'vue-router'
import Header from './components/Header.vue';
import SubNav from './components/SubNav.vue';
import HomeView from './views/HomeView.vue';

import { ref } from 'vue'
import MobileNav from './components/MobileNav.vue';

const displayMenu = ref(true)

// actions
function toggleMenu() {
  displayMenu = !displayMenu
}
</script>

<template>
  <Header></Header>
  
  <span v-if="displayMenu">
    <SubNav @close="displayMenu = false"></SubNav>    
  </span>
  <MobileNav></MobileNav>
  
  <main>
    <RouterView/>   
  </main>
  
</template>