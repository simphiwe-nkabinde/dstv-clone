<script setup>
import IconPlayCircle from './icons/IconPlayCircle.vue';

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
        <btn v-for="item in menuItems" class="border-opacity-20 w-full bg-gray-800 bg-opacity-30 border border-gray-300 border-opacity-20 px-1 py-4 rounded text-center">
            <IconPlayCircle class="w-4 mx-auto"/>
            <span class="text-xs">{{item.name}}</span>
        </btn>
    </div>
</template>