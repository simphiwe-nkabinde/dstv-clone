<script setup>
import IconPlayCircle from './icons/IconPlayCircle.vue';
import IconCart from './icons/IconCart.vue';
import IconClock from './icons/IconClock.vue';
import IconSearch from './icons/IconSearch.vue';
import IconBurger from './icons/IconBurger.vue';

const menuItems = [
    {name: 'Watch', icon: IconPlayCircle},
    {name: 'Buy', icon: IconPlayCircle},
    {name: 'TV Guide', icon: IconPlayCircle},
    {name: 'Search', icon: IconPlayCircle},
    {name: 'Menu', icon: IconPlayCircle}
]

</script>

<template>
    <div class="fixed w-full text-white grid grid-cols-5 gap-2 px-1 justify-items-center bottom-3">
        <button class="border-opacity-20 w-full bg-gray-800 bg-opacity-30 border border-gray-300 border-opacity-20 px-1 py-2 rounded text-center">
            <IconPlayCircle class="w-5 mx-auto"/>
            <span class="text-xs">{{menuItems[0].name}}</span>
        </button>
        <button class="border-opacity-20 w-full bg-gray-800 bg-opacity-30 border border-gray-300 border-opacity-20 px-1 py-2 rounded text-center">
            <IconCart class="w-5 mx-auto"/>
            <span class="text-xs">{{menuItems[1].name}}</span>
        </button>
        <button class="border-opacity-20 w-full bg-gray-800 bg-opacity-30 border border-gray-300 border-opacity-20 px-1 py-2 rounded text-center">
            <IconClock class="w-5 mx-auto"/>
            <span class="text-xs">{{menuItems[2].name}}</span>
        </button>
        <button class="border-opacity-20 w-full bg-gray-800 bg-opacity-30 border border-gray-300 border-opacity-20 px-1 py-2 rounded text-center">
            <IconSearch class="w-5 mx-auto"/>
            <span class="text-xs">{{menuItems[3].name}}</span>
        </button>
        <button @click="$emit('toggle')" class="border-opacity-20 w-full bg-white border border-gray-300 border-opacity-20 px- py-1 rounded text-center text-black">
            <IconBurger class="w-10 mx-auto"/>
            <span class="text-xs">{{menuItems[4].name}}</span>
        </button>
    </div>
</template>