<script setup lang="ts">
import Card from '@/components/Card.vue'
import CardLong from "@/components/CardLong.vue";
import {
  telegramLogo,
  youtubeLogo,
  robotLogo,
  oneSecLogo,
  scamLogo,
  tmailLogo,
  mascanLogo,
  upfileLogo,
  uptimeLogo
} from '@/assets/logo.ts'

const dataForRect: { title: string, description: string, img: string, link:string }[] = [
  {
    title: 'Официальный сайт',
    description: 'Посетите наш официальный сайт, чтобы узнать больше о нас!',
    img: oneSecLogo,
    link: 'https://onesec.uz'
  },
  {
    title: 'YouTube',
    description: 'Посетите наш официальный сайт, чтобы узнать больше о нас!',
    img: youtubeLogo,
    link: 'https://youtube.com/@onesec_uz'
  },
  {
    title: 'Telegram',
    description: 'Посетите наш официальный сайт, чтобы узнать больше о нас!',
    img: telegramLogo,
    link: 'https://t.me/onesec'
  },
  {
    title: 'Telegram Bot',
    description: 'Посетите наш официальный сайт, чтобы узнать больше о нас!',
    img: robotLogo,
    link: 'https://t.me/onesec_bot'
  }]
const dataForLong: { title: string, description: string, img: string,link:string }[] = [
  {
    title: 'SiteUptime',
    description: 'Сервис доступности и мониторинга серверов, веб-сайтов, сервисов, доменов.',
    img: uptimeLogo,
    link: 'https://siteuptime.uz'
  }, {
    title: 'Scam.uz',
    description: 'Сервис доступности и мониторинга серверов, веб-сайтов, сервисов, доменов.',
    img: scamLogo,
    link: 'https://scam.uz'
  }, {
    title: 'Malscan',
    description: 'Сервис доступности и мониторинга серверов, веб-сайтов, сервисов, доменов.',
    img: mascanLogo,
    link: 'https://malscan.uz'
  }, {
    title: 'Tmail.uz',
    description: 'Сервис доступности и мониторинга серверов, веб-сайтов, сервисов, доменов.',
    img: tmailLogo,
    link: 'https://tmail.uz'
  }, {
    title: 'Upfile',
    description: 'Сервис доступности и мониторинга серверов, веб-сайтов, сервисов, доменов.',
    img: upfileLogo,
    link: 'https://upfile.uz'
  }
]
</script>

<template>
  <div class="container mx-auto px-2 bg-gradient-to-r to-indigo-950 from-black flex flex-col items-center justify-center">
    <div class="mt-20"><img src="@/assets/onesec-logo.svg" alt="onesec logo"></div>

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
        <Card :description="data.description" :link="data.link" :title="data.title" :img="data.img"/>
      </div>
    </div>
    <div class="text-4xl font-bold text-center text-white py-12">Наши сервисы</div>

    <div class="space-y-6 last:mb-16">
      <CardLong v-for="data in dataForLong" :title="data.title" :link="data.link" :img="data.img" :description="data.description"/>
    </div>
  </div>
</template>

