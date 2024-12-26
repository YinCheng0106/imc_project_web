<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="flex justify-center mr-6">
    <img class="p-2 mx-2 rounded-xl md:rounded-3xl w-20 h-20 md:w-24 md:h-24" src="../assets/logo.png" alt="TaiChung_Torulogo" />
    <h1 class="py-4 text-bold text-center text-4xl md:text-6xl  dark:text-white mix-md:text-3xl">{{ msg }}</h1>
  </div>
</template>
