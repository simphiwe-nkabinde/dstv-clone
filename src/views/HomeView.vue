<script setup>

const banner = { category: 'news', title: 'The Final Farewell', image: 'queen.jpg', info: 'Seven decades at the helm: A spotlight on her Majesty, Queen Elizabeth II', action: 'Find Out More', actionLink: '/discover/news/60852/queen-elizabeth-ii' }

const promos = [
  { title: 'Internet for everyone', image: '', content: 'NO FIBRE? NO PROBLEM!' },
  { title: 'Unlock yours today', image: '', content: 'Its too easy to get rewarded' },
  { title: 'Get it Today', image: '', content: 'Add movie channels to your package' },
  { title: 'MyDstv App', image: '', content: 'Download the' },
]
</script>

<template>
  <section id="jumbotron" class="text-white px-20 pt-44 pb-2 grid grid-cols-2 grid-rows-2">
    <div>
      <p class="uppercase mb-3 font-bold">{{banner.category}}</p>
      <h1 class="text-5xl font-bold">{{banner.title}}</h1>
      <p class="my-7">{{banner.info}}</p>
      <button
        class="bg-white text-black text-lg py-2 px-8 font-bold rounded-3xl hover:text-white hover:bg-blue-500 transition">{{banner.action}}</button>
    </div>
    <img class="w-72 shadow-xlg skew-x-3 skew-y-3" :src="'src/assets/images/'+banner.image" alt="">
    <div class="mt-20 flex">
      <button v-for="n in 4"
        class="mx-3  text-center rounded-full border-2 p-1 border-transparent hover:border-blue-500 transition">
        <span class="block w-2 h-2 bg-white hover:bg-blue-500 rounded-full"></span>
      </button>
    </div>
  </section>
  <div class="grad-sect"></div>
  <section class="bg-dark-blue text-white">
    <!-- promos -->
    <div class="flex justify-around">
      <div v-for="promo in promos" class="w-48">
        <img src="https://picsum.photos/200" alt="image" class="w-full rounded">
        <div class="absolute inset-0p text-red-500 text-center">
          <p>{{promo.content}}</p>
          <h3>{{promo.title}}</h3>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
#jumbotron {
  background: linear-gradient(90deg, rgb(1, 0, 22) 0%, rgb(1, 1, 54) 55%, rgb(0, 55, 66) 100%), no-repeat right top;
  background-size: contain;
  height: 500px;
}

.grad-sect {
  background: linear-gradient(180deg, rgba(1, 0, 22, 0) 0%, rgb(1, 0, 54) 30%, rgb(1, 0, 22) 100%);
  height: 100px;
  width: 100%;
  margin-top: -30px;
  /* position: relative; */
  /* top: -30px; */
}
.bg-dark-blue {
  background-color: #010017;
  /* box-shadow: 0 0 200px #1c1d25 inset; */
}

</style>