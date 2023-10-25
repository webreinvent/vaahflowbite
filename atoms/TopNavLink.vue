<script setup>
const props = defineProps({
  link:{
    default: '#',
  },
  target:{
    default: null,
  },
  classes:{
    default: 'block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0' +
        ' md:p-0 dark:text-white  dark:hover:bg-gray-700' +
        'dark:hover:text-white md:dark:hover:bg-transparent',
  }
})
</script>
<template>
  <NuxtLink :to="props.link" :target="props.target" :class="props.classes"><slot/></NuxtLink>
</template>
