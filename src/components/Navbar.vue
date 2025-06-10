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
        <div class="  sm:max-w-[1180px] m-auto 0 flex justify-between items-center py-[28px] ">
     <img src="../assets/img/logo.svg" alt="logo" class="block mx-auto sm:mx-0" />
            <ul class="hidden sm:flex sm:gap-[48px] text-[#003459] text-[16px] font-bold">
                <li>Home</li>
                <li>Category</li>
                <li>About</li>
                <li>Contact</li>
            </ul>
            <div class="flex gap-[12px]">
                <img src="../assets/img/Vector.svg" alt="" class="text-right relative right-[70px] top-[-8px] sm:left-[45px] w-[16px] h-[16x]">
                <input type="text" placeholder="Search something here!"
                    class="hidden sm:flex w-[280px] h-[44px] rounded-[46px] bg-white pl-[50px]">
            </div>
            <div class="hidden sm:flex">
                <button class="w-[203px] h-[44px] bg-[#003459] text-white text-[16px]  font-bold rounded-[57px]">Join the
                    community</button>
                <div class="flex gap-[6px]">
                    <img src="../assets/img/Frame.svg" alt="Frame">
                    <p>VNG</p>
                    <img src="../assets/img/Caret_Down.svg" alt="Caret_Down">
                </div>
            </div>
        </div>
        <div class="relative top-[-70px] sm:hidden">
            <img
            src="../assets/img/Hamburger_MD.svg"
            alt="Hamburger_MD"
          @click="active = !active"
          class="cursor-pointer w-8 h-8"
          />
          <div
          v-show="active"
          class="absolute top-10 left-0 bg-[#FFF3D9] px-6 py-4 space-y-2 rounded shadow-lg transition-all duration-300 z-50"
          >
          <div
          class="text-[#002A48] text-[16px] bg-white px-4 py-2 rounded cursor-pointer hover:bg-gray-100 font-semibold"
          v-for="item in dropdowns"
          :key="item"
          @click="handleClick(item)"
          >
          {{ item }}
        </div>
    </div>
</div>
</header>
</template>