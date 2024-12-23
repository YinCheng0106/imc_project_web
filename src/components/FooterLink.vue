<script setup>
import { ref } from 'vue';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faGithub } from '@fortawesome/free-brands-svg-icons';
import { faUpRightFromSquare } from '@fortawesome/free-solid-svg-icons';
let id = 0;
const footerLink = ref([
  {id: id++, name:"Source Code", icon:faGithub, link:"https://github.com/YinCheng0106/imc_project_web"},
  {id: id++, name:"資料來源", icon:faUpRightFromSquare, link:"https://travel.taichung.gov.tw/zh-tw"},
])
</script>

<template>
  <ul class="m-6 list-none grid grid-cols-2">
    <li class="text-center w-full p-1" v-for="footer in footerLink" :key="footer.id">
      <a class="bg-none hover:text-gray-400 dark:text-white dark:hover:text-gray-400" :href="footer.link" target="_blank">
        <FontAwesomeIcon :icon="footer.icon"/> {{ footer.name }}
      </a></li>
  </ul>
</template>
