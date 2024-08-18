<template>
  <main class="flex min-h-screen">
    <TheSidebar class="w-[36%]" />
    <TheMain class="w-[64%]" />
  </main>
</template>

<script setup>
import TheSidebar from './components/sidebar/TheSidebar.vue'
import TheMain from './components/main/TheMain.vue'
import { onMounted } from 'vue'

const { VITE_NAME } = import.meta.env

onMounted(() => {
  document.title = `CV - ${VITE_NAME}`
})
</script>
