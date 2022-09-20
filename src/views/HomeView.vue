<script setup>

const banner = { category: 'news', title: 'The Final Farewell', image: 'queen.jpg', info: 'Seven decades at the helm: A spotlight on her Majesty, Queen Elizabeth II', action: 'Find Out More', actionLink: '/discover/news/60852/queen-elizabeth-ii' }
</script>

<template>
  <section id="jumbotron" class="text-white px-20 pt-44 pb-2">
    <p class="uppercase mb-3 font-bold">{{banner.category}}</p>
    <h1 class="text-5xl font-bold">{{banner.title}}</h1>
    <p class="my-7">{{banner.info}}</p>
    <button class="bg-white text-black text-lg py-2 px-8 font-bold rounded-3xl">{{banner.action}}</button>
    
    <div class="mt-20 flex">
      <button v-for="n in 4" class="text-center hover:bg-blue-500 rounded-full hover:border-2 hover:border-red-500 transition">
        <span class="inline-block w-2 h-2 mr-8 mx-auto bg-white hover:bg-blue-500 rounded-full"></span>
      </button>
    </div>
  </section>
</template>

<style>
#jumbotron {
  background: linear-gradient(90deg, rgb(1, 0, 22) 0%, rgb(1, 1, 54) 55%, rgb(0, 55, 66) 100%), no-repeat right top;
  background-size: contain;
  height: 500px;
}
</style>