<script setup>
import WebTitle from './components/WebTitle.vue'
import AttractionMenu  from './components/AttractionMenu.vue';
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
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

/* @media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / );
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
} */
</style>
