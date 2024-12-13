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
  <ul>
    <li v-for="footer in footerLink" :key="footer.id" class="footerLink"><a :href="footer.link" target="_blank"><FontAwesomeIcon :icon="footer.icon"/> {{ footer.name }}</a></li>
  </ul>
</template>

<style scoped>
  a {
    background-color: none;
  }

  ul {
    margin: 24px;
    list-style: none;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  li {
    text-align: center;
    width: 100%;
    padding: 4px;
  }

  a {
    border-radius: 12px;
  }

  @media (hover:hover){
    a:hover {
      color: rgba(255, 255, 255, 0.7);;
    }
  }

  @media (min-width: 1024px){
    ul {
      display: grid;
      grid-template-columns: 2fr 2fr;
    }

    li {
      width: 100%;
      text-align: center;
    }
  }
</style>
