<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div>
    <h1 class="py-4 text-bold text-center text-6xl">{{ msg }}</h1>
  </div>
</template>
