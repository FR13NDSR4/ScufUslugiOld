<script setup>
defineProps({
  title: String,
  imgUrl: String,
})
</script>

<template>
  <div class="h-16 bg-opacity-70 p-2 bg-blue-500 rounded-md text-white flex items-center text-left font-[Lato-Regular] py-2 justify-between cursor-pointer">
    <div class="flex items-center">
      <img :src="imgUrl" alt="" class="ml-2 mr-0.5" width="35" >
      {{ title }}
    </div>
    <img src="/arrow.svg" alt="" width="30">
  </div>
</template>