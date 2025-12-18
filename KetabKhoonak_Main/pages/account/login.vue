<script setup lang="ts">
const route = useRoute()
definePageMeta({
  layout: false,
  title: "ورود",
  pageTransition: {
    name: 'auth-left'
  }
})

useHead({
  title: `کتابخونک | ${route.meta.title as String}`
})
</script>





<template>
  <div class="w-full h-screen flex justify-center items-center">
    <div class="w-[55%] flex flex-row justify-between ">
      <div class="flex justify-center items-center flex-col p-5">
        <nuxt-link to="/">
          <img src="../../assets/icons/logo.png" class="w-[250px]">
        </nuxt-link>
        <span class="font-peyda font-bold text-xl">ورود</span>
        <span class="font-peyda font-bold text-md text-[#00000099] mt-4">برای ورود فرم زیر را پر کنید</span>        <form action="/" class="flex justify-evenly items-center flex-col my-4 h-[200px]">
          <input type="text" placeholder="نام کاربری" class="w-[330px] py-[13px] px-[42px] outline-none rounded-[20px] font-peyda border border-[#000000B2] bg-transparent placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
          <input type="password" placeholder="رمز" class="w-[330px] py-[13px] px-[42px] outline-none rounded-[20px] font-peyda border border-[#000000B2] bg-transparent placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80">
          <input type="submit" value="تایید" class="w-[330px] py-[13px] px-[42px] bg-[#C0C0C0] rounded-[20px] font-peyda font-medium">
        </form>
        <span class="font-peyda font-medium">ورود شما به معنای پذیرش <span class="text-blue-700 cursor-pointer">شرایط کتابخونک </span> و <span class="text-blue-700 cursor-pointer">قوانین حریم خصوصی</span> است</span>
        <span class="font-peyda font-medium text-md my-2">اکانت ندارید؟ پس <nuxt-link to="/account/signup" class=" text-blue-700"><span>بسازید</span></nuxt-link></span>
        <div class="flex justify-center gap-2 items-center w-full my-4">
          <span class="w-[33%] h-[2px] bg-[#00000080]"></span>
          <span class="font-peyda font-medium">با طریق</span>
          <span class="w-[33%] h-[2px] bg-[#00000080]"></span>
        </div>
        <div class="flex justify-center gap-2 items-center">
          <img class="w-[45px] cursor-pointer" src="../../assets/images/google.png">
          <img class="w-[45px] cursor-pointer" src="../../assets/images/facebook.png">
          <img class="w-[45px] cursor-pointer" src="../../assets/images/linkin.png">
        </div>
      </div>
      <div class="book-img">
        <img class="h-[578px] w-[324px]" src="../../assets/images/img.png">
      </div>
    </div>
  </div>
</template>


<!--
border: 1px solid
background:;
Symbol

-->