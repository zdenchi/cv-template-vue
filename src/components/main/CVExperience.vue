<template>
  <div
    class="relative min-h-0 pl-6 before:absolute before:left-2.5 before:inline-block before:h-[calc(100%-12px)] before:w-px before:translate-x-[2px] before:translate-y-2.5 before:bg-gray-400 before:content-['']"
  >
    <div v-for="exp in expiriences" :key="exp.label" class="relative">
      <h4
        class="mt-3 font-semibold before:absolute before:z-10 before:size-[9px] before:-translate-x-4 before:translate-y-2 before:rounded-full before:border-2 before:border-gray-600 before:bg-white before:content-['']"
      >
        {{ exp.label }}
      </h4>
      <p class="text-xs font-medium text-gray-700">{{ exp.description }}</p>
    </div>
  </div>
</template>

<script setup>
const expiriences = [
  {
    label: 'Senior Web Developer | Company Name | 12.2020 - 12.2023',
    description:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
  },
  {
    label: 'Middle Web Developer | Company Name | 12.2018 - 12.2020',
    description:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
  },
  {
    label: 'Junior Web Developer | Company Name | 01.2016 - 12.2018',
    description:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
  }
]
</script>
