<script setup>
const props = defineProps({
    activeLink: {}
})
</script>

<template>
    <nav class="bg-gray-500 bg-opacity-30 ss-bottom-fast py-2 text-white">
        <ul class="flex justify-center">
            <li v-for="subLink in activeLink.sub"
                class="mx-3 capitalize hover:text-blue-500 transition">
                <RouterLink :to="`/${this.activeLink.main}/${subLink}`">{{subLink}}</RouterLink>
            </li>
        </ul>
    </nav>
</template>