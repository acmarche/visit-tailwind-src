<script setup>
function toggleSearch(action) {
  const menu = document.querySelector("#searchmobile");
  if (action === "close") {
    console.log('close')
    menu.style.display = "hidden"
    menu.style.left = "100%";
  }
  if (action === "open") {
    console.log('open')
    menu.style.left = 0;
  }
}
//pour adapter pour alpinejs
const leftproperty = 'left-full'
</script>
<template>
  <li class="xl:hidden">
    <a href="#" @click.prevent="toggleSearch('open')" class="icon-menu-mobile">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
           stroke="currentColor"
           class="w-6 h-6">
        <path stroke-linecap="round" stroke-linejoin="round"
              d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z"/>
      </svg>
      <span class="text-menu-mobile">Rechercher</span>
    </a>
    <div
        class="xl:hidden absolute bg-white right-0 bottom-[4.5rem] w-full h-[74vh] p-8 transition-all duration-500 overflow-hidden"
        :class="leftproperty"
        id="searchmobile">
      <div class="flex flex-col items-center justify-center px-2">
        <button class="w-32 " @click.prevent="toggleSearch('close')">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
               stroke="currentColor"
               class="w-6 h-6 inline-block text-cta-dark">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
          <span class="font-montserrat-semi-bold text-cta-dark">Fermer</span>
        </button>
        <hr class="border-b border-cta-dark/50 m-3 w-full"/>
        <div class="w-full max-w-lg lg:max-w-xs">
          <label for="search" class="sr-only">Rechercher</label>
          <div class="relative">
            <div class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-3">
              <!-- Heroicon name: mini/magnifying-glass -->
              <svg class="h-5 w-5 text-gray-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                <path fill-rule="evenodd" d="M9 3.5a5.5 5.5 0 100 11 5.5 5.5 0 000-11zM2 9a7 7 0 1112.452 4.391l3.328 3.329a.75.75 0 11-1.06 1.06l-3.329-3.328A7 7 0 012 9z" clip-rule="evenodd" />
              </svg>
            </div>
            <input id="search" name="search" class="block w-full rounded-md border border-gray-300 bg-white py-2 pl-10 pr-3 leading-5 placeholder-gray-500 focus:border-indigo-500 focus:placeholder-gray-400 focus:outline-none focus:ring-1 focus:ring-indigo-500 sm:text-sm" placeholder="Chercher" type="search">
          </div>
        </div>
      </div>
    </div>
  </li>
</template>