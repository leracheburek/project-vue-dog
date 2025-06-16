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
    <header class=" bg-[#FCEED5] ">
        <div
            class="bg-[#F7DBA7] w-[635px] h-[635px] rotate--25_23 rounded-[99px] absolute top-[-607px] left-[-143.33px] z-0 ">
        </div>
        <div class="max-w-[414px] xl:max-w-[1180px] m-auto relative z-10 ">
            <div class="flex justify-between items-center py-7 ">
                <img src="../assets/img/logo.svg" alt="logo" class="block mx-auto xl:mx-0 " />
                <ul class="hidden xl:flex gap-12 text-accent text-4 font-bold ">
                    <li>Home</li>
                    <li>Category</li>
                    <li>About</li>
                    <li>Contact</li>
                </ul>
                <div class="xl:hidden absolute">
                    <img src="../assets/img/Hamburger_MD.svg" alt="Hamburger_MD" @click="active = !active" />
                    <div v-show="active" class="absolute top-10 bg-[#FFF3D9]">
                        <div class="text-accent text-[16px] bg-white px-4 py-2 rounded " v-for="item in dropdowns"
                            :key="item" @click="handleClick(item)">
                            {{ item }}
                        </div>
                    </div>
                </div>
                <div class="hidden xl:flex">
                    <img src="../assets/img/Vector.svg" alt="Vector"
                        class="text-right relative right-[70px] xl:left-[30px] xl:top-[15px] w-4 h-4">
                    <input type="text" placeholder="Search something here!"
                        class="hidden xl:flex w-[280px] h-[44px] rounded-[46px] bg-white pl-[50px] border-none outline-none">
                </div>
                <div class="hidden xl:flex items-center gap-[14px]">
                    <button class="w-[203px] h-[44px] bg-accent text-white text-4 font-bold rounded-[57px]">Join the
                        community</button>
                    <div class="flex gap-[6px]">
                        <img src="../assets/img/Frame.svg" alt="Frame" class="w-[21px] h-[21px]">
                        <p>VNG</p>
                        <img src="../assets/img/Caret_Down.svg" alt="Caret_Down" class="w-[24px] h-[24px]">
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>