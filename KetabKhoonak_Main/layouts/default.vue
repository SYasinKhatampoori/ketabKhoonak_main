<script setup lang="ts">

</script>

<template>
  <div class="w-full h-screen flex flex-col space-between items-center bg-[#FED8B1]">
  <header class="relative w-full h-[100px] bg-[#E4C09B] flex justify-center gap-x-[900px] items-center">

    <!--    menu-->
    <div class="flex flex-col items-center justify-center w-[68px] h-[68px] bg-[#CBA985] rounded-full cursor-pointer">
      <img class="w-[42px] h-[42px]" src="../assets/icons/menu-svgrepo-com.svg" alt="">
    </div>
    <!--    logo-->
    <div class="absolute">
      <img src="../assets/icons/logo.png" class="w-[200px] ">
    </div>
    <!--    buttons-->
    <div class="flex justify-evenly items-center w-[379px]">
      <button class="font-peyda font-bold text-[20px]
      bg-[#CBA985] py-[20px] px-[5px] rounded-[10px]
       shadow-[inset_0_3px_0_0_#00000040,inset_0_-3px_0_0_#00000040]
      outline-none">ورود و ثبت نام</button>
      <button class="font-peyda font-bold text-[20px]
bg-[#E4C09B]  py-[20px] px-[5px] rounded-[10px]
shadow-[inset_0_3px_0_0_#00000040,inset_0_-3px_0_0_#00000040]
 outline-none">کتابخانه من</button>
    </div>
  </header>
  <main>
    <slot/>
  </main>
  <footer class="absolute bottom-0 w-full h-[318px] bg-[#987B5E] flex justify-evenly items-center ">
<!--    about us-->
    <div class=" flex justify-center items-start flex-col w-auto p-5 h-[194px] border-l-4 border-[#00000080]">
      <img src="../assets/icons/logo.png" class="w-[200px] ">
      <h1 class="w-[382px] font-peyda font-medium text-white text-[20px] text-start">اواسط سال ۱۴۰۴، چند جوان پرانرژی
        و ایده‌پرداز دور هم جمع شدیم
        تا یک کار خیری را از رویا به واقعیت تبدیل کنیم.  ما تصمیم گرفتیم برای کتابخانه‌هایی
        که تازه شروع به فعالیت کرده‌اند،
        سایت‌هایی زیبا و کاربرپسند طراحی کنیم.</h1>
    </div>
<!--    contact us-->
    <div class="font-peyda font-medium h-[194px] text-[20px] p-5 text-white flex justify-center items-start flex-col w-auto border-l-4 border-[#00000080]">
      <div class="flex flex-col items-center justify-center">
        <span>09121234567</span>
      </div>
      <div class="flex flex-col items-center justify-center">
        <span>قم|خیابان رسالت|کوچه 3|هنرستان نمونه دولتیگیوچی</span>
      </div>
      <div class="flex flex-col items-center justify-center">
        <span>Bookworm@gmail.com</span>
      </div>
    </div>
<!--    idon`t know-->
    <div class="flex flex-col items-center justify-evenly p-5 h-[194px] w-auto font-peyda font-medium text-white text-[18px]">
      <div class="grid grid-cols-3 grid-rows-2 gap-x-5 gap-y-5">
        <h1>انتقادات و پیشنهادات</h1>
        <h1>دربارکتابخونک</h1>
        <h1>همکاری درفروش</h1>
        <h1>سوالات متداول</h1>
        <h1>قوانین و مقررات</h1>
        <h1>تماس باما</h1>
      </div>
      <div class="flex flex-col items-center justify-center">
        <h1 class="font-peyda font-bold">کتابخونک را در شبکه‌های اجتماعی دنبال کنید:</h1>
        <div>

        </div>
      </div>
    </div>
  </footer>
  </div>
</template>

<style scoped>

</style>


<!--
box-shadow: 0px 3px 0px 0px #00000040 inset;

box-shadow: 0px -3px 0px 0px #00000040 inset;

box-shadow: 0px 3px 0px 0px #00000040 inset;

box-shadow: 0px -3px 0px 0px #00000040 inset;
#00000080
-->