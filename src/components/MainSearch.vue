<script setup>
import TipSearchButton from '@/components/TipSearchButton.vue'

const listTips = [
  "Танки",
  "Загранпаспорт",
  "Лицевой счёт СКФ",
  "Запись к КВД",
  "Регистрация ТС"
]
</script>

<template>
  <div class="bg-gradient-to-b from-blue-700 via-blue-600 to-blue-500 h-2/5 grid p-1">
    <div class="flex p-1 mt-5">
      <button class="bg-opacity-70 bg-blue-500 ml-2 m-1 p-1 pt-2 rounded-md text-white flex items-stretch text-left">
        <img src="/elections.svg" alt="" class="ml-2" width="35" >
        Быть или не быть скуфом
        <img src="/arrow.svg" alt="" width="30">
      </button>
      <button class="bg-opacity-70 bg-blue-500 m-1 p-2 rounded-md text-white flex items-stretch text-left">
        <img src="/flag.svg" alt="flag" class="mx-1">
        Флаги в продаже
        <img src="/arrow.svg" alt="" width="30">
      </button>
    </div>
    <div class="relative">
      <img src="/robot.svg" alt="" width="35" class="absolute left-6 top-5" >
      <input
        type="text"
        placeholder="Введите запрос..."
        class="ml-3 mt-3 w-11/12 rounded-xl p-3.5 outline-none pl-14"
      />
      <img src="/plane.svg" alt="" width="30" class="absolute right-9 top-6" />
    </div>
    <div class="flex-wrap flex gap-3 mt-4 ml-3 mb-7">
      <TipSearchButton
        v-for="title in listTips"
        :key="title"
        :title="title"
      />
    </div>
  </div>
</template>