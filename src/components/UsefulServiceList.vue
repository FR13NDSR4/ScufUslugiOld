<script setup>
  import UsefulService from '@/components/UsefulService.vue'

  const services = [
    {
      img: "/decide_together.svg",
      title: "Скуфуслуги Решаем вместе",
      description: "Задайте вопрос, подайте жалобу, внесите предложение",
      link: "mailto:ppr229339@gmail.com?subject=Скуфуслуги Решаем вместе"
    },
    {
      img: "/loudspeaker.svg",
      title: "Общественные голосования",
      description: "Учавствуйте в жизни скуфов: голосуйте, делитесь мнением",
      link: "#"
    },
    {
      img: "/hand_braille.svg",
      title: "Скуфам с инвалидностью",
      description: "Справки, образения, льготы, услуги для реабилитации",
      link: "#"
    },
    {
      img: "/auto.svg",
      title: "Скуфуслуги Танк",
      description: "Электронные документы и сервисы для танковладельцев",
      link: "#"
    },
    {
      img: "/child.svg",
      title: "Рождение скуфа",
      description: "Первые документы, детский сад, пособия и другие услуги",
      link: "#"
    },
  ]
</script>

<template>
  <div class="bg-[#fafcff]">
    <div class="m-4">
      <h1 class="text-2xl"><b>Полезные сервисы</b></h1>
      <div class="grid">
        <div class="mt-4 rounded-2xl p-7 grid bg-gradient-to-r from-lime-800 via-lime-600 to-lime-500 cursor-pointer">
          <h1
            class="text-2xl text-bold text-white text-left pr-4 font-[Lato-Bold]">
            <b>Получите свою Альтушку</b>
          </h1>
          <p
            class="text-white text-md mt-3 pr-4 font-[Lato-Regular]">
            Заполните анкету и получите свою Альтушку
          </p>
        </div>
      </div>
      <UsefulService
        v-for="service in services"
        :key="service.img"
        :imgUrl="service.img"
        :title="service.title"
        :description="service.description"
        :link="service.link"
      />
    </div>
  </div>
</template>
