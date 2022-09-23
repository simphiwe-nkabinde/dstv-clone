<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'
import SubNavVue from './SubNav.vue'
import SearchIcon from './icons/IconSearch.vue'
import UserIcon from './icons/IconUser.vue'
import SubNav from './SubNav.vue'

const activeLink = ref(0)

</script>
    
<template>
    <div class="fixed w-full">
        <header class="bg-black grid grid-cols-3 text-gray-300 py-5 px-2 items-center">
            <div class="justify-self-start block h-5 w-5 mx-1 grid grid-cols-3 grid-rows-3 gap-1 self-center group">
                <span v-for="n in 9" class="w-1 h-1 bg-white group-hover:bg-gray-200 transition"></span>
            </div>
            <RouterLink to="/">
                <img alt="" class="justify-self-center" src="@/assets/images/logo.svg" width="70" />
            </RouterLink>
            <nav aria-label="sub navigation" class="justify-self-end flex items-center">
                <!-- <SearchIcon class="w-7 mx-2 hover:text-blue-500 transition" /> -->
                <UserIcon class="w-8 mx-2 hover:text-blue-500 transition" />
                <RouterLink to="/signin" class="mx-2 capitalize hover:text-blue-500 transition">sign in</RouterLink>
            </nav>
        </header>
        <div class="tracking-widest p-2 text-white text-xs bg-black bg-opacity-30 backdrop-blur-15 border border-gray-700 border-opacity-30 shadown text-center">OPEN MENU</div>
    </div>
</template>