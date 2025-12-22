<script setup lang="ts">


const route = useRoute()
definePageMeta({
  title: "پنل ادمین",
  layout: false,
})

useHead({
  title:`کتابخونک | ${route.meta.title as String}`
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
<div class="w-full h-screen flex justify-center items-center flex-col p-y-20">
  <div class="flex flex-col justify-center items-center w-[1143px] h-[280px] bg-[#7F654C] rounded-[20px] py-[16px] px-[55px] shadow-[0_20px_60px_-15px_rgba(0,0,0,0.6)]">
    <div class="w-[733px] h-[157px] flex flex-col items-center justify-center">

      <div
          class="w-[713px] h-[39px] border-b border-[#BAC6D3]
           font-medium text-[14px]
           flex items-center justify-center gap-x-5 text-[#BAC6D3]"
      >
        <div
            v-for="tab in tabs"
            :key="tab.id"
            @click="activeTab = tab.id"
            class="h-full cursor-pointer flex items-center px-2
             border-b-2 transition-all duration-200"
            :class="
        activeTab === tab.id
          ? 'border-yellow-500 text-yellow-500'
          : 'border-transparent text-[#BAC6D3]'
      "
        >
          <span>{{ tab.label }}</span>
        </div>
      </div>

    </div>
  </div>
</div>
</template>



<!--
box-shadow: 0px 0px 40px -10px #00000080;

-->