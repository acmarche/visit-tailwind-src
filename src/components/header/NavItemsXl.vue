<script setup>
defineEmits(["open-search"]);
</script>
<template>
  <li class="hidden xl:list-item border-transparent pb-2 nav-top-xl">
    <a href="#">Accueil</a>
  </li>
  <li class="hidden xl:list-item border-transparent pb-2 nav-top-xl">
    <a href="#">Inspirations</a>
  </li>
  <li class="hidden xl:list-item border-transparent pb-2 nav-top-xl">
    <a href="#">Agenda</a>
  </li>
  <li class="hidden xl:list-item border-transparent pb-2 nav-top-xl group relative">
    <a href="#" class="inline-flex items-center text-white">S'organiser
     <svg class="text-white ml-2 h-5 w-5 group-hover:text-gray-500" xmlns="http://www.w3.org/2000/svg"
             viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
          <path fill-rule="evenodd"
                d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                clip-rule="evenodd"/>
        </svg>
    </a>
    <ul class="invisible rounded-md group-hover:visible absolute bg-white font-montserrat-medium text-caractere px-3 py-1 top-11 transition-all duration-500 ease-in-out">
      <li class="before:triangle before:left-10 hover:text-cta-light py-2">
        <a href="#" class="p-2">Découvrir</a>
      </li>
      <li class="hover:text-cta-light py-2">
        <a href="#" class="p-2">Savourer</a>
      </li>
      <li class="hover:text-cta-light py-2">
        <a href="#" class="p-2">Bouger</a>
      </li>
      <li class="hover:text-cta-light py-2">
        <a href="#" class="p-2">Séjourner</a>
      </li>
      <li class="hover:text-cta-light py-2">
        <a href="#" class="p-2">MICE</a>
      </li>
    </ul>
  </li>
  <li class="hidden xl:list-item border-transparent pb-2 nav-top-xl">
    <a href="#">Pratique</a>
  </li>
  <li class="hidden xl:list-item border-transparent pb-2 nav-top-xl">
    <a href="#" @click.prevent="$emit('open-search')">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
        <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z" />
      </svg>
    </a>
  </li>
</template>
<style>
li.nav-top-xl {
  @apply transition-all duration-300 ease-in-out hover:border-b-4 hover:border-cta-light
}
</style>