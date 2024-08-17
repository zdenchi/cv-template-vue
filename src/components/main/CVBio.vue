<template>
  <div class="h-[288px] px-10 pt-14">
    <p class="text-3xl font-semibold">{{ VITE_NAME }}</p>
    <p class="font-medium">{{ VITE_POSITION }}</p>
  </div>
</template>

<script setup>
const { VITE_NAME, VITE_POSITION } = import.meta.env
</script>
