<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'
import SubNavVue from './SubNav.vue'
import SearchIcon from './icons/IconSearch.vue'
import UserIcon from './icons/IconUser.vue'
import SubNav from './SubNav.vue'

const activeLink = ref(0)

const links = [
    { main: 'watch', sub: ['stream-now', 'live-tv', 'tv-shows', 'movies', 'sport', 'kids', 'tv-guide', 'boxOffice', 'showmax'] },
    { main: 'discover', sub: ['tv-guide', 'highlights', 'loving-local', 'best-of-international', 'kids', 'behind-the-screens', 'sport', 'news'] },
    { main: 'buy' },
    { main: 'rewards' },
    { main: 'myDstv' },
    { main: 'help', sub: ['fix-errors', 'how-to-watch', 'how-to-play', 'find-an-installer', 'find-an-agency', 'faqs', 'contact-us'] }
]

</script>
    
<template>
    <div class="fixed w-full">
        <header class="bg-black flex justify-between text-gray-300 px-10 py-5 items-center">
            <div class="flex items-center">
                <RouterLink to="/">
                    <img alt="" class="" src="@/assets/images/logo.svg" width="125" />
                </RouterLink>
                <div class="block h-5 w-5 mx-5 grid grid-cols-3 grid-rows-3 gap-1 self-center group">
                    <span v-for="n in 9" class="w-1 h-1 bg-gray-500 group-hover:bg-gray-200 transition"></span>
                </div>

                <nav aria-label="main navigation">
                    <ul class="flex font-light">
                        <li v-for="link in links" @click="activeLink = link"
                            class="ss-right mx-2 capitalize hover:text-blue-500 transition">
                            <RouterLink :to="`/${link.main}`">{{link.main}}</RouterLink>
                        </li>
                    </ul>
                </nav>
            </div>

            <nav aria-label="sub navigation" class="flex items-center font-light">
                <SearchIcon class="w-7 mx-2 hover:text-blue-500 transition" />
                <UserIcon class="w-8 mx-2 hover:text-blue-500 transition" />
                <RouterLink to="/signin" class="mx-2 capitalize hover:text-blue-500 transition">sign in</RouterLink>
            </nav>
        </header>
        <SubNav v-if="activeLink.sub" :active-link="activeLink"></SubNav>
    </div>
</template>