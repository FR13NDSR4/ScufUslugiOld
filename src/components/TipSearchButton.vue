<script setup>
defineProps({
  title: String
})
</script>

<template>
  <button
    class="p-2 rounded-tl rounded-r-2xl rounded-b-2xl bg-blue-700 px-4 text-white">
    {{ title }}
  </button>
</template>