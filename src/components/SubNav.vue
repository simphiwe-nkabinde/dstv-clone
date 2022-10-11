<script setup>
import data from '../assets/data.json';
import IconX from './icons/IconX.vue';

const navLinks = data.navList;


</script>

<template>
    <div class="absolute w-full h-5/6 p-2 ss-top-fast">
        <nav class="px-5 py-3 rounded h-full bg-black bg-opacity-60 border border-gray-300 border-opacity-20 text-white overflow-x-scroll">
            <button @click="$emit('close')" class="float-right text-white">
                <IconX class="w-6 fixed right-5"></IconX>
            </button>
            <div class="grid grid-cols-2 gap-3">
                <ul v-for="links in navLinks" class="mb-5">
                    <h2 class="font-bold text-xl border-b border-gray-300 border-opacity-20 pb-2">{{links.main}}</h2>
                    <li v-for="link in links.sub" class="my-2">
                        <RouterLink :to="`/${link}`">{{link}}</RouterLink>
                    </li>
                </ul>                
            </div>

        </nav>
    </div>

</template>