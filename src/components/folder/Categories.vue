<script setup>
import { onMounted, ref } from "vue";

const categories = ref([]);

function getCats() {
  fetch("https://visitmarche.be/api/categories.php?id=4")
    .then(function(response) {
      // The API call was successful!
      return response.json();
    })
    .then(function(data) {
      // This is the JSON from our response
      categories.value = data;
    })
    .catch(function(err) {
      // There was an error
      console.warn("Something went wrong.", err);
    });
}

onMounted(() => {
  getCats();
});
</script>
<template>
  <ul class="xl:flex pt-6 flex-1 flex-wrap gap-2 xl:w-1/2 my-2 mx-auto">
    <li
      v-for="item in categories"
      :key="item.cat_ID"
      class="border border-cta-dark p-3 font-montserrat-light hover:bg-cta-light hover:text-white">
      <a
        :href="item.url"
        class="">
        {{ item.name }}
      </a>
    </li>
  </ul>
</template>