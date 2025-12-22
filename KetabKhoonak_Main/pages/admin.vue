<script setup lang="ts">
import AdminCart from '@/components/Admin.vue';
import AdminCountCart from '@/components/AdminCount.vue';


import amanatImage from '@/assets/images/admin/amanat.png'
import amanatCountImage from '@/assets/images/admin/amanatCounnt.png'
import bookCountImage from '@/assets/images/admin/bookCount.png'
import MKetabImage from '@/assets/images/admin/mKetab.png'
import memberImage from '@/assets/images/admin/memberCount.png'
import McountImage from '@/assets/images/admin/modiriat.png'
import AdminCount from '@/components/AdminCount.vue';





const route = useRoute()
definePageMeta({
  title: "پنل ادمین",
  layout: false,
})

useHead({
  title: `کتابخونک | ${route.meta.title as String}`
})

const activeTab = ref('smart')

const tabs = [
  { id: 'smart', label: 'جستجوی هوشمند' },
  { id: 'title', label: 'عنوان' },
  { id: 'author', label: 'نویسنده' },
  { id: 'publisher', label: 'ناشر' },
  { id: 'subject', label: 'موضوع' },
]
</script>

<template>
  <div class="w-full h-screen flex justify-center items-center gap-7 flex-col">
    <div
      class="flex flex-col justify-center items-center w-[1143px] h-[250px] bg-[#7F654C] rounded-[20px] py-[16px] px-[55px] shadow-[0_10px_60px_-15px_rgba(0,0,0,0.6)]">
      <div class="w-[733px] h-[157px] flex flex-col items-center justify-evenly">

        <div class="w-[713px] h-[39px] border-b border-[#BAC6D3]
           font-medium text-[14px]
           flex items-center justify-center gap-x-5 text-[#BAC6D3]">
          <div v-for="tab in tabs" :key="tab.id" @click="activeTab = tab.id" class="h-full cursor-pointer flex items-center px-2
             border-b-2 transition-all duration-200" :class="activeTab === tab.id
                ? 'border-yellow-500 text-yellow-500'
                : 'border-transparent text-[#BAC6D3]'
              ">
            <span>{{ tab.label }}</span>
          </div>
        </div>
        <form v-if="activeTab === 'smart'" class="w-[535px] h-[50px] rounded-[20px] flex justify-center items-center">
          <input class="bg-[#FFEAD4] rounded-r-full h-full w-[120.54000091552734px] flex items-center cursor-pointer"
            type="submit" value="جست و جو">
          <span class="w-[2px] h-full bg-black"></span>
          <input
            class="w-[414px] bg-[#FED8B1] h-full rounded-l-full outline-none p-5 placeholder:font-peyda placeholder:font-medium placeholder:text-black placeholder:opacity-80"
            type="text" placeholder="عبارت مد نظر را جستجو کنید">
        </form>
      </div>
    </div>
    <div class="w-[1143px] grid grid-cols-3 gap-x-[114px] gap-y-[60px]">
      <AdminCart lable="مدیریت کتاب ها " :url="MKetabImage" />
      <AdminCart lable="مدیریت اعضا" :url="memberImage" />
      <AdminCart lable="میز امانات" :url="amanatCountImage" />
      <AdminCountCart lable="تعداد کل کتاب ها" :url="bookCountImage"/>
      <AdminCountCart lable="تعداد کل اعضا" :url="McountImage"/>
      <AdminCountCart lable="تعداد کل امانات" :url="amanatCountImage"/>
    </div>
  </div>
</template>



<!--
box-shadow: 0px 0px 40px -10px #00000080;

-->