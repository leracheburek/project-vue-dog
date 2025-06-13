<script setup>
import { ref } from 'vue'

const active = ref(false)

const dropdowns = ['Home', 'Category', 'About', 'Contact']

const selectedVal = ref(dropdowns[0])

const handleClick = (item) => {
    selectedVal.value = item
    active.value = false
}
</script>

<template>
    <header class=" bg-[#FCEED5]">
        <div
            class="max-w-[414px] xl:max-w-[1180px] mb:w-full mb:max-w-[768px]  m-auto 0 sm:flex gap-5 justify-between items-center py-7 ">
            <img src="../assets/img/logo.svg" alt="logo" class="block mx-auto xl:mx-0 " />
            <ul class="hidden xl:flex gap-12 text-accent text-4 font-bold ">
                <li>Home</li>
                <li>Category</li>
                <li>About</li>
                <li class="hidden xl:flex">Contact</li>
            </ul>
            <div class="hidden xl:flex gap-[12px] relative ">
                <img src="../assets/img/Vector.svg" alt=""
                    class="text-right relative right-[70px] xl:left-[45px] xl:top-[15px] w-4 h-4 ">
                <input type="text" placeholder="Search something here!"
                    class="hidden xl:flex w-[280px] h-[44px] rounded-[46px] bg-white pl-[50px] border-none outline-none ">
            </div>
            <div class="hidden xl:flex">
                <button class="w-[203px] h-[44px] bg-accent text-white text-4 font-bold rounded-[57px]">Join the
                    community</button>
                <div class="flex gap-[6px] mt-[10px] ml-[14px]">
                    <img src="../assets/img/Frame.svg" alt="Frame" class="w-[21px] h-[21px]">
                    <p>VNG</p>
                    <img src="../assets/img/Caret_Down.svg" alt="Caret_Down" class="w-[24px] h-[24px]">
                </div>
            </div>
        </div>
        <div class="relative top-[-70px] xl:hidden  max-w-[414px] m-auto">
            <img src="../assets/img/Hamburger_MD.svg" alt="Hamburger_MD" @click="active = !active"
                class="cursor-pointer w-8 h-8 ml-[30px]" />
            <div v-show="active"
                class="absolute top-10 left-0 bg-[#FFF3D9] px-6 py-4 space-y-2 rounded shadow-lg transition-all duration-300 z-50">
                <div class="text-accent text-[16px] bg-white px-4 py-2 rounded cursor-pointer hover:bg-gray-100 font-semibold"
                    v-for="item in dropdowns" :key="item" @click="handleClick(item)">
                    {{ item }}
                </div>
            </div>
        </div>
    </header>
</template>