<script setup>
import TipSearchButton from '@/components/TipSearchButton.vue'
import BigTipSearchList from '@/components/BigTipSearchList.vue'

const listTips = [
  "Танки",
  "Загранпаспорт",
  "Лицевой счёт СКФ",
  "Запись к КВД",
  "Регистрация ТС"
]
</script>

<template>
  <div class="bg-gradient-to-b from-blue-700 via-blue-600 to-blue-500 pt-1 pb-1">
    <BigTipSearchList/>
    <div class="relative ml-1 mt-2">
      <img src="/robot.svg" alt="" width="35" class="absolute left-6 top-5" >
      <input
        type="text"
        placeholder="Введите запрос..."
        class="ml-3 mt-3 w-11/12 rounded-xl p-3.5 outline-none pl-14 font-[Lato-Regular]"
      />
      <img src="/plane.svg" alt="" width="30" class="absolute right-9 top-6" />
    </div>
    <div class="flex-wrap flex gap-3 mt-4 ml-4 mb-7">
      <TipSearchButton
        v-for="title in listTips"
        :key="title"
        :title="title"
      />
    </div>
  </div>
</template>