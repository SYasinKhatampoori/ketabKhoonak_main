<template>
  <div class="w-full h-[110px] flex flex-col justify-evenly  border-b-2 border-[#00000080] my-4">

    <div class="w-full flex justify-between items-center">
      <span>{{ name }}</span>

      <div class="flex gap-1">
        <img
          v-for="i in 5"
          :key="i"
          :src="i <= stars ? fullStar : emptyStar"
          class="w-[12px] h-[12px]"
          alt="star"
        />
      </div>
    </div>

    <span class="text-sm">{{ comment }}</span>
  </div>
</template>

<script setup lang="ts">
import fullStar from '@/assets/icons/fullstar.svg'
import emptyStar from '@/assets/icons/emptystar.svg'

defineProps<{
  name: string
  stars: number // 1 تا 5
  comment: string
}>()
</script>
