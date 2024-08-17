<template>
  <div class="pl-10">
    <h3 class="border-b py-1.5 text-xl font-semibold">{{ title }}</h3>

    <ul
      class="mt-3 flex flex-col gap-1 text-pretty text-xs font-medium"
      v-bind="$attrs"
      v-if="list.length"
    >
      <li v-for="li in list" :key="li" class="pr-2.5">{{ li }}</li>
      <slot name="li" />
    </ul>

    <slot />
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  list: {
    type: Array,
    default: () => []
  }
})
</script>
