<script setup>
//https://www.getrevue.co/profile/shrutibalasa/issues/where-is-inline-flex-used-1394402
const tags = [{name: 'Actualités', id: 1}, {name: 'Infos travaux', id: 2}]
</script>
<template>
  <ul class="flex flex-wrap gap-2">
    <li v-for="item in tags" :key="item.id"
        class="text-sm mx-2 whitespace-nowrap flex items-center border border-caractere text-caractere transition-all duration-500 ease-in-out hover:bg-cta-light hover:text-white"
    >
      <a href="/" class="px-2 py-2 ">{{ item.name }}</a>
    </li>
  </ul>
</template>
