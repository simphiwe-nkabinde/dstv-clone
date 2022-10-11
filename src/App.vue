<script setup>
import { RouterView } from 'vue-router'
import Header from './components/Header.vue';
import SubNav from './components/SubNav.vue';
import HomeView from './views/HomeView.vue';

import { ref } from 'vue'
import MobileNav from './components/MobileNav.vue';

const displayMenu = ref(true)

</script>

<template>
  <Header></Header>
  
  <span v-if="displayMenu">
    <SubNav @close="displayMenu = false"></SubNav>    
  </span>
  <MobileNav @toggle="displayMenu = !displayMenu" :display="displayMenu"></MobileNav>
  
  <main>
    <RouterView/>   
  </main>
  
</template>