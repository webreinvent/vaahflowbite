<script setup>
const props = defineProps({
  link:{
    default: '#',
  },
  target:{
    default: null,
  },
  classes:{
    default: 'py-2 hover:bg-red-200 px-3 bg-red-100 text-gray-900 rounded' +
        ' dark:text-white  dark:hover:bg-gray-700' +
        'dark:hover:text-white md:dark:hover:bg-transparent',
  }
})
</script>
<template>
  <NuxtLink :to="props.link" :target="props.target" :class="props.classes"><slot/></NuxtLink>
</template>
