
<template>
  <div>
    <label class="relative inline-flex items-center mb-5 cursor-pointer">
      <input type="checkbox" value="true" v-model="isDark" @click="isDark = !isDark" class="sr-only peer">
      <div class="w-9 h-5 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 dark:peer-focus:ring-blue-800 rounded-full peer dark:bg-gray-700 peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-4 after:w-4 after:transition-all dark:border-gray-600 peer-checked:bg-blue-600"></div>
      <span class="ml-3 text-sm font-medium text-gray-900 dark:text-gray-300">Small toggle {{head.htmlAttrs.class}}</span>
    </label>
  </div>
</template>
<script setup>
import { watch, ref, reactive } from 'vue'

let isDark = ref(true);

let head = reactive({
  htmlAttrs:{
    class: 'dark'
  },
  bodyAttrs: {
    class: 'dark:bg-primary dark:text-white'
  }
});

watch(isDark , async function (newVal, oldVal) {
  if(newVal){
    head.htmlAttrs.class = 'dark';
  } else{
    head.htmlAttrs.class = '';
  }
});

useHead(head);

</script>
