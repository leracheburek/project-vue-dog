<script setup>
import { ref } from 'vue';
import Dog1 from '../assets/img/dog1.svg';
import Dog2 from '../assets/img/dog2.svg';
import Dog3 from '../assets/img/dog3.svg';
import Dog4 from '../assets/img/dog4.svg';
import Dog5 from '../assets/img/dog5.svg';
import Dog6 from '../assets/img/dog6.svg';
import Dog7 from '../assets/img/dog7.svg';
import Dog8 from '../assets/img/dog8.svg';
import ButtonLera from './ui/ButtonLera.vue';
const dogs = ref([
    {
        id: 1,
        name: "MO231 - Pomeranian White",
        gene: "Gene:Male",
        age: "Age: 02 mouths",
        mony: "6.900.000 VND",
        img: Dog1
    },
    {
        id: 2,
        name: "MO502 - Poodle Tiny Yellow",
        gene: "Gene:Female",
        age: "Age: 02 mouths",
        mony: "3.900.000 VND",
        img: Dog2
    },
    {
        id: 3,
        name: "MO102 - Poodle Tiny Sepia",
        gene: "Gene:Male",
        age: "Age: 02 mouths",
        mony: "4.000.000 VND",
        img: Dog3
    },
    {
        id: 4,
        name: "MO512 - Alaskan Malamute Grey",
        gene: "Gene:Male",
        age: "Age: 03 mouths",
        mony: "8.900.000 VND",
        img: Dog4
    },
    {
        id: 5,
        name: "MO231 - Pembroke Corgi Cream",
        gene: "Gene:Male",
        age: "Age: 03 mouths",
        mony: "7.900.000 VND",
        img: Dog5
    },
    {
        id: 6,
        name: "MO502 - Pembroke Corgi Tricolor",
        gene: "Gene:Female",
        age: "Age: 02 mouths",
        mony: "6.900.000 VND",
        img: Dog6
    },
    {
        id: 7,
        name: "MO102 -  Pomeranian Grey",
        gene: "Gene:Male",
        age: "Age: 02 mouths",
        mony: "6.500.000 VND",
        img: Dog7
    },
    {
        id: 8,
        name: "MO512 - Poodle Tiny Dairy Cow",
        gene: "Gene:Male",
        age: "Age: 03 mouths",
        mony: "5.000.000 VND",
        img: Dog8
    }
])

</script>

<template>
    <section class="bg-white mt-[40px]">
        <div class="max-w-[414px] xl:max-w-[1180px]  m-auto  justify-between flex-col-reverse">
            <div class="flex xl:justify-between ">
                <div class="mb-[28px]">
                    <p class="text-[14px] xl:text-[16px] font-medium ">Whats new?</p>
                    <h1 class="text-[20px] xl:text-[24px] font-bold text-[#003459] ">Take a look at some of our pets
                    </h1>
                </div>

                <ButtonLera type="border" class="xl:flex hidden ">
                    View more
                    <img src="../assets/img/arrow-right.svg" alt="arrow-right">
                </ButtonLera>
            </div>

            <div class="grid xl:grid-cols-4 gap-5  grid-cols-2">
                <div class=" p-2 bg-[#FDFDFD] border border-gray-100 rounded-[12px]" v-for="dog in dogs" :key="dog.id">
                    <img :src="dog.img" :alt="dog.name" class="w-full rounded-[12px]" />
                    <div>
                        <p class="text-[12px] md:text-[14px] xl:text-[16px] font-bold pt-3">{{ dog.name }}</p>
                        <p class="text-[10px] md:text-[12px] xl:text-[14px] text-accent-dog font-medium">{{ dog.gene }}
                        </p>
                        <p class="text-[10px] md:text-[12px] xl:text-[14px] text-accent-dog font-medium">{{ dog.age }}
                        </p>
                        <p class="text-[12px]  md:text-[14px] xl:text-[16px] font-bold">{{ dog.mony }}</p>
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>