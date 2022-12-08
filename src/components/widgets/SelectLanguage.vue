<script setup>
const languages = [
  {
    id: 1,
    name: 'Français',
    url: '/fr',
    img: 'https://visitmarche.be/wp-content/plugins/sitepress-multilingual-cms/res/flags/fr.png'
  },
  {
    id: 1,
    name: 'English',
    url: '/en',
    img: 'https://visitmarche.be/wp-content/plugins/sitepress-multilingual-cms/res/flags/en.png'
  },
  {
    id: 1,
    name: 'Dutch',
    url: '/nl',
    img: 'https://visitmarche.be/wp-content/plugins/sitepress-multilingual-cms/res/flags/nl.png'
  },
]
</script>
<template>

  <div class="grid place-items-center	">
    <ul class="flex flex-col gap-4">
      <li class="p-3" v-for="item in languages" :key="item.id">
        <a :href="item.url" class="flex flex-row items-center gap-2">
          <img :src="item.img" alt="" class="w-6 h-6"/>
          <span>{{ item.name }}</span>
        </a>
      </li>
    </ul>
  </div>

</template>