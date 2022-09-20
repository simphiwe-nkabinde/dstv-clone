<script setup>
const props = defineProps({
    activeLink: {}
})
</script>

<template>
    <nav class="bg-gray-800 bg-opacity-30 ss-bottom-fast py-2 text-white absolute w-full">
        <ul class="flex justify-center">
            <li v-for="subLink in activeLink.sub"
                class="mx-3 ss-center capitalize hover:text-blue-500 transition">
                <RouterLink :to="`/${this.activeLink.main}/${subLink}`">{{subLink}}</RouterLink>
            </li>
        </ul>
    </nav>
</template>

<style>
nav {
    backdrop-filter: blur(5px);
}
</style>