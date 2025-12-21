<script setup lang="ts">
defineProps({
  title: String,
  url: String,
})
</script>

<template>
  <div class="w-[142px] h-[181px] flex justify-evenly items-center flex-col cursor-pointer">
    <div class="w-full h-[142px] rounded-full border-[6px] border-[#7F654C] bg-[#CBA985] flex flex-col justify-center items-center">
      <img class="w-[74px] h-[74px]" :src="url">
    </div>
    <h1 class="font-peyda font-medium text-[20px]">{{ title }}</h1>
  </div>
</template>

<style scoped>

</style>