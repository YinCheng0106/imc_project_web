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
      <Moon class="text-gray-200" v-if="isDark" />
      <Sun v-else />
    </button>
  </div>
</template>
