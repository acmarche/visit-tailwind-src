<template>
  <ul class="mx-2 xl:mx-4 font-montserrat-semi-bold text-white xl:flex xl:items-start -z-10">
    <li class="xl:list-item border-transparent pb-2 nav-top-xl group relative">
      <a href="#" class="inline-flex items-center text-white">FR
        <svg class="text-white ml-2 h-5 w-5 group-hover:text-gray-500" xmlns="http://www.w3.org/2000/svg"
             viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
          <path fill-rule="evenodd"
                d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                clip-rule="evenodd"/>
        </svg>
      </a>
      <ul class="invisible rounded-md bg-white text-caractere my-4 h-24 absolute top-7 flex flex-col justify-center items-center group-hover:visible transition-all duration-500 ease-in-out">
        <li class="hover:text-cta-light before:triangle">
          <a href="#" class="p-4">FR</a>
        </li>
        <li class="hover:text-cta-light">
          <a href="#" class="p-4">NL</a>
        </li>
        <li class="hover:text-cta-light">
          <a href="#" class="p-4">EN</a>
        </li>
      </ul>
    </li>
  </ul>
</template>