<script setup>
import { RouterLink} from 'vue-router'
import SearchIcon from './icons/IconSearch.vue'
import UserIcon from './icons/IconUser.vue'

const mainLinks = ['watch', 'discover', 'buy', 'rewards', 'myDstv', 'help']

</script>
    
<template>
    <header class="bg-black flex justify-between text-gray-300 px-10 py-8 items-center">
        <div class="flex items-center">
            <RouterLink to="/">
                <img alt="" class="" src="@/assets/images/logo.svg" width="125" />
            </RouterLink>
            <div class="block h-5 w-5 mx-5 grid grid-cols-3 grid-rows-3 gap-1 self-center group">
                <span v-for="n in 9" class="w-1 h-1 bg-gray-500 group-hover:bg-gray-200"></span>
            </div>

            <nav aria-label="main navigation">
                <ul class="flex font-light">
                    <li v-for="link in mainLinks" class="mx-2 capitalize hover:text-blue-500">
                        <RouterLink :to="`/${link}`">{{link}}</RouterLink>
                    </li>
                </ul>
            </nav>
        </div>

        <nav aria-label="sub navigation" class="flex items-center font-light">
            <SearchIcon class="w-7 mx-2 hover:text-blue-500" />
            <UserIcon class="w-8 mx-2 hover:text-blue-500" />
            <RouterLink to="/signin" class="mx-2 capitalize hover:text-blue-500">sign in</RouterLink>
        </nav>
    </header>
</template>