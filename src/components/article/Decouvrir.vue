<script setup>
const icones2 = [
  {id: 1, nom: 'Patrimoine', image: '/wp-content/themes/visittail/assets/tartine/eglise-decouvrir.png', url: '/fr/?cat=9'},
  {id: 2, nom: 'Arts', image: '/wp-content/themes/visittail/assets/tartine/statue-decouvrir.png', url: '/fr/?cat=10'},
  {id: 3, nom: 'Balades', image: '/wp-content/themes/visittail/assets/tartine/sac-dos-decouvrir.png', url: '/fr/?cat=11'},
  {id: 4, nom: 'Gourmandises', image: '/wp-content/themes/visittail/assets/tartine/chou-decouvrir.png', url: '/fr/?cat=13'},
  {id: 5, nom: 'Fêtes', image: '/wp-content/themes/visittail/assets/tartine/tambour-decouvrir.png', url: '/fr/?cat=12'},
]
const icones = [
  {id: 1, nom: 'Patrimoine', image: 'images/eglise-decouvrir.png', url: '/fr/?cat=9'},
  {id: 2, nom: 'Arts', image: 'images/statue-decouvrir.png', url: '/fr/?cat=10'},
  {id: 3, nom: 'Balades', image: 'images/sac-dos-decouvrir.png', url: '/fr/?cat=11'},
  {id: 4, nom: 'Gourmandises', image: 'images/chou-decouvrir.png', url: '/fr/?cat=13'},
  {id: 5, nom: 'Fêtes', image: 'images/tambour-decouvrir.png', url: '/fr/?cat=12'},
]
// /wp-content/themes/visittail/assets/tartine/eglise-decouvrir.png
</script>
<template>
  <ul class="list-none decouvrir-page flex flex-col flex-wrap justify-center pt-4 mx-auto w-2/3">
    <li class="group w-40text-center pt-3" v-for="item in icones" :key="item.id">
      <a :href="item.url" class="flex items-center justify-start ml-auto  rounded-lg shadow-lg cat-pat">
        <figure>
          <img :src="item.image" class="w-32" alt="">
        </figure>
        <span class="text-cta-dark text-lg group-hover:text-cta-light">{{ item.nom }}</span>
        <span class="mr-12 ml-auto group-hover:text-cta-light">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
               stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12h15m0 0l-6.75-6.75M19.5 12l-6.75 6.75"/>
          </svg>
        </span>
      </a>
    </li>
  </ul>
</template>