<script setup lang="ts">
const route = useRoute();
definePageMeta({
  title: "پروفایل",
})
useHead({
  title: `کتابخونک | ${route.meta.title as String}`,
})
</script>

<template>
  <div class="flex justify-center items-center flex-col w-full my-4 gap-5">
    <div class="flex items-start justify-center flex-col w-[1046.5px] border-b border-[#00000080]">
      <h1 class="mb-1">ویرایش مشخصات من</h1>
    </div>
    <div class="flex items-center justify-start w-[1046.5px]">
      <img src="../assets/images/img.png" class="w-[152px] h-[152px] rounded-full">
      <div class="flex items-center justify-start cursor-pointer">
        <img src="../assets/images/camera.png" class="w-[51px] h-[51px]]">
        <span class="font-peyda font-medium">ویرایش عکس</span>
      </div>
    </div>
    <form action="/" class="flex items-center justify-start w-[1046.5px] flex-col relative">
      <div class="flex flex-row justify-between items-center">
        <div class="flex justify-evenly items-center flex-col gap-y-[63px]">
          <input placeholder="نام" type="text" class="w-[430px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
          <input placeholder="شماره تلفن" type="text" class="w-[430px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
        </div>
        <div class="mx-10 flex justify-center items-center">
          <span class="h-[276.64801025390625px] w-[1px] bg-[#00000080] "></span>
        </div>
        <div class="flex justify-evenly items-center flex-col gap-y-[63px]">
          <input placeholder="نام کاربری" type="text" class="w-[430px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
          <input placeholder="ایمیل" type="text" class="w-[430px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
        </div>
      </div>

      <div class="flex justify-end items-center flex-row gap-x-3 w-[940.5px]">
        <button class="w-[170px]  h-[48px] py-[8px] px[16px] bg-transparent border border-[#00000099] rounded-[12px] flex items-center justify-center gap-3  text-black">
          <span>انصراف</span>
        </button>
        <button class="w-[170px] h-[48px] py-[8px] px[16px] bg-[#7F654C] rounded-[12px] flex items-center justify-center gap-3  text-[#FFFFFF]">
          <span>ذخیره اطلاعات</span>
          <img src="../assets/icons/check.svg" class="w-[17.59000015258789px]">
        </button>
      </div>
    </form>
  </div>
</template>


<!--<form class="w-[1046px] flex items-center justify-center flex-col">
      <div class="flex items-center justify-start w-[1046.5px] ">
        <div class="flex items-center justify-center flex-col">
          <input placeholder="نام خانوادگی" type="text" class="w-[330px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
          <input placeholder="نام خانوادگی" type="text" class="w-[330px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
        </div>
        <div class="flex items-center justify-evenly flex-col ">
          <input placeholder="نام خانوادگی" type="text" class="w-[330px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
          <input placeholder="نام خانوادگی" type="text" class="w-[330px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
        </div>
      </div>

    </form>-->