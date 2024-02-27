<script setup lang="ts">
import Card from '@/components/Card.vue'
import oneSecLogo from '@/assets/onesec-logo-sm.png'
import CardLong from "@/components/CardLong.vue";

const dataForRect: { title: string, description: string, img: string }[] = [
  {
    title: 'Официальный сайт',
    description: 'Посетите наш официальный сайт, чтобы узнать больше о нас!',
    img: oneSecLogo
  },
  {
    title: 'YouTube',
    description: 'Посетите наш официальный сайт, чтобы узнать больше о нас!',
    img: oneSecLogo
  },
  {
    title: 'Telegram',
    description: 'Посетите наш официальный сайт, чтобы узнать больше о нас!',
    img: oneSecLogo
  },
  {
    title: 'Telegram Bot',
    description: 'Посетите наш официальный сайт, чтобы узнать больше о нас!',
    img: oneSecLogo
  }]
</script>

<template>
  <div class="container px-2 bg-gradient-to-r to-indigo-950 from-black flex flex-col items-center justify-center z-50">
    <div class="mt-24"><img src="@/assets/onesec-logo.svg" alt="onesec logo"></div>

    <div class="mb-12">
      <div class="relative self-center mt-14 text-4xl font-bold text-center text-white whitespace-nowrap">
        Наша Сеть:
      </div>
      <div class="relative self-center mt-5 text-base text-center text-white whitespace-nowrap">
        Исследуйте Все Ресурсы и Социальные Сети!
      </div>
    </div>
    <div class="grid grid-cols-2 gap-2">
      <div v-for="data in dataForRect">
        <Card :description="data.description" :title="data.title" :img="data.img"/>
      </div>
    </div>
    <div class="text-4xl font-bold text-center text-white py-12">Наши сервисы</div>

    <div class="space-y-6 last:mb-16">
      <CardLong v-for="data in dataForRect" :title="data.title" :img="data.img" :description="data.description"/>
    </div>
  </div>
</template>

