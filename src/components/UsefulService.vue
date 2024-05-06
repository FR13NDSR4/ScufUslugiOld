<script setup>
const props = defineProps({
  title: String,
  description: String,
  imgUrl: String,
  link: String
})

const openLink = () => {
  window.open(props.link, '_self')
}
</script>

<template>
  <div class="shadow-[0_1px_8px_rgb(0,0,0,0.1)] rounded-2xl p-7 mt-10 cursor-pointer" @click="openLink">
    <img :src="imgUrl" alt="" width="40">
    <h1 class="text-md text-black mt-3"><b>{{ title }}</b></h1>
    <p class="text-slate-600 text-md mt-3">{{ description }}</p>
  </div>
</template>
