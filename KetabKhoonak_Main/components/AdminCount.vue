<template>
  <div class="relative w-[305px] h-[164px] bg-[#987B5E] rounded-[20px]
  flex justify-evenly items-center flex-col
  ">
    <img class="w-[67px] h-[67px]" :src="url">
    <span class="text-[30px] text-[#FFFFFF]">{{ lable }}</span>
    <span class="absolute w-[159px] h-[48px] rounded-[30px] bg-[#CBA985]
    bottom-[-16%]
    ">{{ count }}</span>
  </div>
</template>

<script lang="ts" setup>
defineProps({
    lable: String,
    url: String,
    count: Number,
})
</script>

<style>

</style>