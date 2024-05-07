<script setup>
defineProps({
  title: String
})
</script>

<template>
  <div
    class="cursor-pointer p-2 rounded-tl rounded-r-2xl rounded-b-2xl bg-blue-700 px-4 text-white font-[Lato-Regular]">
    {{ title }}
  </div>
</template>