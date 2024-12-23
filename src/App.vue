<script setup>
import WebTitle from './components/WebTitle.vue'
import AttractionMenu  from './components/AttractionMenu.vue';
import FooterLink from './components/FooterLink.vue';
import DarkMode from './components/DarkMode.vue';
</script>

<template >
  <header>
    <div>
      <WebTitle class="my-4" msg="魅力台中" />
      <DarkMode class="absolute m-4 top-2 right-2" />
    </div>
  </header>
  <main >
    <AttractionMenu />
  </main>
  <footer>
    <FooterLink />
  </footer>
</template>

<style scoped>
.logo {
  display: block;
  margin: 0 auto 2rem;
}
</style>
