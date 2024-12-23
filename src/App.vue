<script setup>
import WebTitle from './components/WebTitle.vue'
import AttractionMenu  from './components/AttractionMenu.vue';
import FooterLink from './components/FooterLink.vue';
import DarkMode from './components/DarkMode.vue';
</script>

<template >
  <header>
    <div>
      <WebTitle msg="魅力台中" />
      <DarkMode class="absolute top-2 right-2" />
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
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
</style>
