<script setup lang="ts">
defineProps({
  url:String,
  nashr: String,
})
</script>

<template>
  <div class="cursor-pointer w-[183px] h-[318px] rounded-[18px] bg-[#E4C09B] flex flex-col justify-evenly items-center">
    <div class="flex flex-col justify-center items-start">
      <img :src="url" class="w-[163px] h-[206px] rounded-[10px] bg-center bg-cover">
    </div>
    <span class="w-full h-[10px] bg-[#FFEAD4]"></span>
    <div class="flex flex-row justify-center items-center w-[90%]">
      <p class="text-[16px] text-[#7F654C]">{{ nashr }}</p>
    </div>
  </div>
</template>

<style scoped>

</style>