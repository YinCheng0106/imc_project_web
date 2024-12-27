<script setup>
  import { useDark, useToggle } from '@vueuse/core'
  import { Sun, Moon } from 'lucide-vue-next';
  const isDark = useDark({
    valueDark: 'dark',
    valueLight: 'light',
  })
  const toggleDark = useToggle(isDark)
</script>

<template>
  <div>
    <button
      @click="toggleDark()"
      class="p-2 m-2"
    >
      <Moon class="text-gray-300 hover:text-white" v-if="isDark" />
      <Sun class="text-black hover:text-gray-400" v-else />
    </button>
  </div>
</template>
