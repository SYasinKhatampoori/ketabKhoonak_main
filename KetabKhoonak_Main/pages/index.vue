<script setup lang="ts">
import Header from '@/components/Header.vue'
import Cart from '@/components/Carts.vue'
import Nashr from '@/components/Nasherin.vue'

import  NashrImage from '@/assets/images/Nashr.png'
import librari from "@/assets/icons/librari.png"
import libImage from "@/assets/images/librari.png"


import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Autoplay } from 'swiper/modules'

import 'swiper/css'
import 'swiper/css/navigation'

import slider1 from '@/assets/images/slider1.png'
import slider2 from '@/assets/images/slider2.png'
import slider3 from '@/assets/images/slider3.png'

const slides = [slider1, slider2, slider3]

const route = useRoute()
definePageMeta({ title: 'خانه' })
useHead({ title: `کتابخونک | ${route.meta.title as string}` })
</script>

<template>
<div class="w-[100%] my-10 flex flex-col justify-evenly h-[3200px] items-center">
  <div class="relative w-[1296px] h-[335px] bg-center bg-cover rounded-[20px] flex flex-col justify-center items-center bg-[url('.././assets/images/librari.png')]">
    <div class="flex justify-center items-center rounded-[10px] border border-[#000000] px-2 bg-[#EAD8C0]">
      <img src=".././assets/icons/search-svgrepo-com.svg" class="w-[20px] h-[20px]">
      <input class="w-[494px] h-[44px] rounded-[10px] outline-none bg-[#EAD8C0] p-5 placeholder:text-black placeholder:opacity-75" type="search" placeholder="جستجوی کتاب، نویسنده و...">
    </div>
    <div class="absolute bottom-[-77%] h-full flex justify-center gap-[32px] flex-row">

      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
    </div>
  </div>
  <div class="w-[1296px] flex justify-evenly items-center flex-row gap-[21px] mt-20">
    <ClientOnly>
      <div class="relative w-[957px] h-[546px] mx-auto">
        <Swiper
            dir="rtl"
            :modules="[Navigation, Autoplay]"
            :autoplay="{ delay: 4000, disableOnInteraction: false }"
            loop
            :navigation="{ nextEl: '.hero-next', prevEl: '.hero-prev' }"
            class="w-full h-full rounded-[26px] overflow-hidden"
        >
          <SwiperSlide
              v-for="(img, index) in slides"
              :key="index"
          >
            <img
                :src="img"
                class="w-full h-full object-cover"
            />
          </SwiperSlide>
        </Swiper>

        <!-- فلش راست -->
        <button
            class="hero-next absolute right-6 top-1/2 -translate-y-1/2 z-10 bg-white/20 backdrop-blur rounded-full p-3"
        >
          ❮
        </button>

        <!-- فلش چپ -->
        <button
            class="hero-prev absolute left-6 top-1/2 -translate-y-1/2 z-10 bg-white/20 backdrop-blur rounded-full p-3"
        >
          ❯
        </button>
      </div>
    </ClientOnly>

    <div class="w-[318px] h-[546px] rounded-[18px] bg-[#E4C09B] flex flex-col justify-evenly items-center">
      <h1 class="font-bold text-[24px] text-[#A32708]">منتخب سال</h1>
      <div class="flex flex-col justify-center items-center">
        <img src=".././assets/images/about3.jpg" class="w-[257px] h-[324px] rounded-[10px]">
        <h1 class="font-bold text-[24px] text-[#4C3B2A]">شاهزاده کوچولو</h1>
      </div>
      <span class="w-full h-[10px] bg-[#FFEAD4]"></span>
      <div class="flex flex-row justify-between items-center w-[90%]">
        <p class="text-[16px] text-[#7F654C]">نشر چشمه</p>
        <div class="flex flex-row justify-center gap-1 items-center">
          <img src=".././assets/icons/star-svgrepo-com.svg" class="w-[25px] h-[25px]">
          <span>4</span>
        </div>
      </div>
    </div>
  </div>
  <div class="w-[1296px] flex justify-evenly   items-center h-[500px] flex-col">
    <div class="w-full flex justify-between items-center">
      <h1 class="font-bold text-[32px] text-[#4C3B2A]">جدید ترین کتاب ها</h1>

      <nuxt-link to="/" class="text-[#65503A] text-[20px]">مشاهده همه ></nuxt-link>
    </div>
    <div class="flex flex-row justify-evenly items-center w-full gap-5">
      <Cart title="مرا ببوس" stars="5" :url="libImage" nashr="علی" nevisande="محمد"/>
      <Cart title="مرا ببوس" stars="5" :url="libImage" nashr="علی" nevisande="محمد"/>
      <Cart title="مرا ببوس" stars="5" :url="libImage" nashr="علی" nevisande="محمد"/>
      <Cart title="مرا ببوس" stars="5" :url="libImage" nashr="علی" nevisande="محمد"/>
      <Cart title="مرا ببوس" stars="5" :url="libImage" nashr="علی" nevisande="محمد"/>
      <Cart title="مرا ببوس" stars="5" :url="libImage" nashr="علی" nevisande="محمد"/>
    </div>
  </div>
  <div class="w-[1296px] flex justify-evenly   items-center h-[500px] flex-col">
    <div class="w-full flex justify-between items-center">
      <h1 class="font-bold text-[32px] text-[#4C3B2A]">دسته بندی ها</h1>
    </div>
    <div class="grid grid-cols-7 w-full gap-5">
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
      <Header title="رمان" :url="librari"/>
    </div>
  </div>
  <div class="w-[1296px] flex justify-evenly   items-center h-[500px] flex-col">
    <div class="w-full flex justify-between items-center">
      <h1 class="font-bold text-[32px] text-[#4C3B2A]">ناشرین</h1>

      <nuxt-link to="/" class="text-[#65503A] text-[20px]">مشاهده همه ></nuxt-link>
    </div>
    <div class="flex flex-row justify-evenly items-center w-full gap-5">
      <Nashr :url="NashrImage" nashr="علی"/>
      <Nashr :url="NashrImage" nashr="علی"/>
      <Nashr :url="NashrImage" nashr="علی"/>
      <Nashr :url="NashrImage" nashr="علی"/>
      <Nashr :url="NashrImage" nashr="علی"/>
      <Nashr :url="NashrImage" nashr="علی"/>
    </div>
  </div>
</div>
</template>

<style scoped>

</style>