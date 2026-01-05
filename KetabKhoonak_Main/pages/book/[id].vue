<template>
    <div class="w-full h-[1000px] my-[10px] flex justify-center items-start">
        <div class="w-full px-[43px] grid grid-cols-2 gap-x-[400px]">
            <div class="w-[809px] h-[434px] rounded-[20px] bg-[#B19271] flex justify-between items-center p-8">
                <img src="../../assets/images/librari.png" class="w-[228px] h-[306px] rounded-[20px]" alt="">
                <div class="w-[400px] flex justify-center gap-y-5 items-center flex-col">
                    <div class="flex justify-between items-center w-full  border-b-[3px] border-[#00000080]">
                        <h1 class="text-[26px] text-[#FFEAD4]">شاهزاده کوچولو</h1>
                        <div class=" w-[50px] flex justify-evenly items-center">
                            <img :src="fullStar" alt="" class="w-[26.16666793823242px] h-[26.16666793823242px]">
                            <span class="text-[#4C3B2A] font-bold">3</span>
                        </div>
                    </div>
                    <div class="w-full h-[100px] border-b-[3px] border-[#00000080]">

                    </div>
                    <button class="w-[430px] h-[64px] bg-[#FFEAD4] text-[#4C3B2A] rounded-[20px]">امانت گرفتن</button>
                </div>
            </div>
            <div class="w-[497px]  h-[589px] flex justify-evenly  items-center flex-col bg-[#B19271] rounded-[25px] p-5 ">
                <form action=""
                    class="w-[397px] flex   h-[530px] justify-evenly items-start flex-col p-3 text-[#FFFBF7]">
                    <span>نظر شما درباره این کتاب</span>
                    <textarea name="details" placeholder="توضیحات مربوط را وارد کنید"
                        class="bg-[#B19271] outline-none border-[2px] border-black w-full h-[200px] rounded-[20px] placeholder:text-black p-3 text-black"></textarea>
                </form>
                
                <span class="text-[#FFFFFF]">نقد ها و امتیازات </span>
                <Comment name="علی اکبری" stars="4" comment="خوب بود" />
                <Comment name="علی اکبری" stars="2" comment="خوب بود" />
                <span class="text-[#FFFFFF] my-5 cursor-pointer">نمایش همه</span>
            </div>
            
        </div>
    </div>
</template>


<script lang="ts" setup>
import Comment from '~/components/Comment.vue';
import fullStar from '@/assets/icons/fullstar.svg'

const router = useRouter()
definePageMeta({

    title: "مشخصات کتاب",
})
const book = {

    title: 'شاهزده کوچولو',
    author: 'آنتوان دوسنت اگزوپری',
    translator: 'شبنم مهدی پور',
    punlisher: 'نگاه',
    stars: '3',
    bCode: 142485,
    shabak: 978 - 6223321047,
}


</script>

<style></style>

<!-- 
نسکافه ای/60 -->