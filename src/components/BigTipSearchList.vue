<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import BigTipSearch from '@/components/BigTipSearch.vue'

const listTips = [
  {
    title:"Быть или не быть скуфом",
    imgUrl:"/elections.svg"
  },
  {
    title:"Купить флаги",
    imgUrl:"/flag.svg"
  },
  {
    title:"Конкурсы для юных скуфов",
    imgUrl:"/star.svg"
  },
]

const YesOrNo = () => {
  const randomInt = Math.floor(Math.random() * 2);
  if (randomInt === 1) {
    alert("Да, быть")
  } else {
    alert("Нет, не быть")
  }
}
</script>

<template>
  <div class="mt-6">
    <swiper
      class="flex"
      :slides-per-view="1.5"
      :space-between="10">

      <swiper-slide class="ml-4" @click="YesOrNo()">
        <BigTipSearch
          :title="listTips[0].title"
          :imgUrl="listTips[0].imgUrl"
        />
      </swiper-slide>
      <swiper-slide>
        <BigTipSearch
          :title="listTips[1].title"
          :imgUrl="listTips[1].imgUrl"
        />
      </swiper-slide>
      <swiper-slide>
        <BigTipSearch
          :title="listTips[2].title"
          :imgUrl="listTips[2].imgUrl"
        />
      </swiper-slide>

    </swiper>
  </div>
</template>