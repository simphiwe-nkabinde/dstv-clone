<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'

const mainLinks = ['watch', 'discover', 'buy', 'rewards', 'myDstv', 'help']

</script>

<template>
  <header class="bg-gray-900 flex text-gray-200 px-10 py-9">
    <img alt="" class="" src="@/assets/images/logo.svg" width="125" height="125" />
    <div class="block h-5 w-5 mx-5 grid grid-cols-3 grid-rows-3 gap-1 self-center group">
      <span v-for="n in 9" class="w-1 h-1 bg-gray-500 group-hover:bg-gray-200"></span>
    </div>
    <div>
      <nav class="flex">
        <ul class="flex font-light">
          <li v-for="link in mainLinks" class="mx-2 capitalize hover:text-blue-500">
            <RouterLink :to="`/${link}`">{{link}}</RouterLink>
          </li>
        </ul>
        <ul class="">
          <RouterLink to="/signin">Sign in</RouterLink>
          <RouterLink to="/signin">Sign in</RouterLink>
        </ul>
      </nav>
    </div>
  </header>

  <RouterView />
</template>