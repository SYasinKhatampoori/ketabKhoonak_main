<template>
  <div class="w-[305px] h-[164px] bg-[#987B5E] rounded-[20px] cursor-pointer
  flex justify-evenly items-center flex-col
  ">
    <img class="w-[67px] h-[57px]" :src="url">
    <span class="text-[30px] text-[#FFFFFF]">{{ lable }}</span>
  </div>
</template>

<script lang="ts" setup>
defineProps({
    lable: String,
    url: String
})
</script>

<style>

</style>