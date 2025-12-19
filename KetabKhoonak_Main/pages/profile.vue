<script setup lang="ts">
const route = useRoute();
definePageMeta({
  title: "پروفایل",
})
useHead({
  title: `کتابخونک | ${route.meta.title as String}`,
})

const name = ref('')
const phone = ref('')
const username = ref('')
const email = ref('')

const edit = ref(false) // پیش‌فرض false

watch([name, phone, username, email], () => {
  edit.value =
      name.value.trim() !== '' &&
      phone.value.trim() !== '' &&
      username.value.trim() !== '' &&
      email.value.trim() !== ''
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
          <input v-model="name" placeholder="نام" type="text"
                 class="w-[430px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:text-black placeholder:opacity-75" />

          <input v-model="phone" placeholder="شماره تلفن" type="text"
                 class="w-[430px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:text-black placeholder:opacity-75" />
        </div>

        <div class="mx-10 flex justify-center items-center">
          <span class="h-[276px] w-[1px] bg-[#00000080]"></span>
        </div>

        <div class="flex justify-evenly items-center flex-col gap-y-[63px]">
          <input v-model="username" placeholder="نام کاربری" type="text"
                 class="w-[430px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:text-black placeholder:opacity-75" />

          <input v-model="email" placeholder="ایمیل" type="text"
                 class="w-[430px] p-[12px] border border-[#000000B2] bg-transparent rounded-[20px] outline-none placeholder:text-black placeholder:opacity-75" />
        </div>
      </div>

      <div class="flex justify-end items-center flex-row gap-x-3 w-[940.5px]">
        <button
            class="w-[170px] h-[48px] bg-transparent border border-[#00000099] rounded-[12px] flex items-center justify-center text-black placeholder:text-black placeholder:opacity-75">
          انصراف
        </button>

        <button
            :class="edit ? 'bg-[#4C3B2A] text-white' : 'bg-[#7F654C] text-white'"
            class="w-[170px] h-[48px] rounded-[12px] flex items-center justify-center gap-3 transition"
            :disabled="!edit"
        >
          <span>ذخیره اطلاعات</span>
          <img src="../assets/icons/check.svg" class="w-[17px]" />
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