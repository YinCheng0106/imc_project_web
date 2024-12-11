<script setup>
import WebTitle from './components/WebTitle.vue'
import AttractionMenu  from './components/AttractionMenu.vue';
import FooterLink from './components/FooterLink.vue';
</script>

<template>
  <header>
    <div class="wrapper">
      <WebTitle msg="魅力台中" />
    </div>
  </header>

  <main>
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
