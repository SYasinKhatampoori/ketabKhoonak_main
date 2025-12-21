<script setup lang="ts">
defineProps({
  title: String,
  stars: Number,
  url: String,
  nashr: String,
  nevisande: String,
})
</script>

<template>
  <div class="cursor-pointer w-[183px] h-[318px] rounded-[18px] bg-[#E4C09B] flex flex-col justify-evenly items-center">
    <div class="flex flex-col justify-center items-start">
      <img :src="url" class="w-[163px] h-[206px] rounded-[10px] bg-center bg-cover">
      <h1 class="font-medium text-[17px] text-[#4C3B2A]">{{ title }}</h1>
      <span class="text-[10px] text-[#7F654C]">{{ nevisande }}</span>
    </div>
    <span class="w-full h-[10px] bg-[#FFEAD4]"></span>
    <div class="flex flex-row justify-between items-center w-[90%]">
      <p class="text-[16px] text-[#7F654C]">{{ nashr }}</p>
      <div class="flex flex-row justify-center gap-1 items-center">
        <img src=".././assets/icons/star-svgrepo-com.svg" class="w-[25px] h-[25px]">
        <span class="text-[10px] text-[#7F654C]">{{ stars }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>