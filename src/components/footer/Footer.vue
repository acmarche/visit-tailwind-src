<script setup>
import ShortCut from "@/components/footer/ShortCut.vue";
import Copyright from "@/components/footer/Copyright.vue";
import IconesSocial from "@/components/header/IconesSocial.vue";
</script>
<template>
  <footer
      class="flex flex-col justify-between bg-caractere p-5 pb-20 font-montserrat-light text-white xl:grid xl:grid-cols-4 xl:pb-5"
  >
    <div class="flex gap-2">
      <a href="/fr" class="">
        <img src="/images/visit_logo.png"
             alt="logo visit" class="w-20 h-12" loading="lazy"/>
      </a>
      <a href="https://www.marche.be" class=""
         title="template">
        <img src="/images/marche_logo.png"
             alt="logo ville" class="w-20 h-12" loading="lazy"/>
      </a>
    </div>
    <div class="border-l border-l-white/50 px-3">
      <h4 class="font-montserrat-semi-bold">Menu</h4>
      <ul class="grid grid-cols-2 p-2 text-sm leading-6 xl:grid-cols-1">
        <li class="px-2">
          <a href="https://visitmarche.be/fr/categorie/inspirations/">Inspirations</a>
        </li>
        <li class="px-2">
          <a href="https://visitmarche.be/fr/categorie/sorganiser/">S'organiser</a>
        </li>
        <li class="px-2">
          <a href="https://visitmarche.be/fr/categorie/agenda/">Agenda</a>
        </li>
        <li class="px-2">
          <a href="https://visitmarche.be/fr/categorie/pratique/">Pratique</a>
        </li>
      </ul>
    </div>
    <ShortCut/>
    <div class="border-l border-l-white/50 px-3">
      <h4 class="font-montserrat-semi-bold">Contact</h4>
      <div class="mb-2 text-sm leading-6">
        Office Communal du Tourisme<br/>
        <a href="tel:+3284326946">+32(0)84 32 69 46</a><br/>
        Du lundi au jeudi : de 8h à 12h et de 13h à 17h<br/>
        Vendredi : de 8h à 12h et de 13h à 15h<br/>
      </div>
      <IconesSocial/>
    </div>
    <Copyright/>
  </footer>
</template>
