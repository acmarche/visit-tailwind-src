<script setup>
const icones = [
  {id: 1, nom: 'Patrimoine', image: 'images/eglise-decouvrir.png', url: '/'},
  {id: 2, nom: 'Arts', image: 'images/statue-decouvrir.png', url: '/'},
  {id: 3, nom: 'Balades', image: 'images/sac-dos-decouvrir.png', url: '/'},
  {id: 4, nom: 'Gourmandises', image: 'images/chou-decouvrir.png', url: '/'},
  {id: 5, nom: 'Fêtes', image: 'images/tambour-decouvrir.png', url: '/'},
]
</script>
<template>
  <ul class="decouvrir-page flex flex-col flex-wrap justify-center pt-4 mx-auto w-2/3">
    <li class="group w-40text-center pt-3" v-for="item in icones" :key="item.id">
      <a :href="item.url" class="flex items-center justify-start ml-auto  rounded-lg shadow-lg cat-pat">
        <figure>
          <img :src="item.image" class="w-36" alt="">
        </figure>
        <span class="text-cta-dark text-lg group-hover:text-cta-light">{{ item.nom }}</span>
      </a>
    </li>
  </ul>
</template>