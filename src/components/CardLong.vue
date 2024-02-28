<script setup lang="ts">
defineProps<{
  title: string
  description: string
  img: string
  link:string
}>()
function toLink(link: string) {
  window.open(link, '_blank')
}
</script>

<template>
  <div @click="toLink(link)"
      class="flex transition duration-300 ease-in-out hover:scale-105 cursor-pointer gap-5 bg-transparent justify-between px-10 py-7 text-white rounded-3xl border border-solid backdrop-blur-[5px] bg-black bg-opacity-50 border-white border-opacity-70"
  >
    <img
        alt="onesec-logo-sm"
        loading="lazy"
        :src="img"
        class=" aspect-[3.85] w-[73px]"
    />
    <div class="flex flex-col flex-1">
      <div class="text-sm font-bold">{{ title }}</div>
      <div class="mt-2.5 text-xs">
        {{ description }}
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>