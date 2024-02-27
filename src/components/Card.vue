<script setup lang="ts">
defineProps<{
  title: string
  description: string
  img: string
}>()
</script>

<template>
  <div class="flex flex-col flex-1 py-6 pr-8 pl-3.5 rounded-3xl border border-solid backdrop-blur-[2px] bg-black bg-opacity-30 border-white border-opacity-50"
  >
    <div class="w-fit p-2 rounded-full bg-white bg-opacity-20">
      <img
          loading="lazy"
          alt="onesec-logo-sm"
          :src="img"
          class="w-7 "
      />
    </div>
    <div class="mt-5 text-sm font-bold text-white">{{ title }}<br/></div>
    <div class="mt-4 text-xs text-white">
      {{ description }}
    </div>
  </div>
</template>

<style scoped>

</style>