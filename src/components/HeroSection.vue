<script setup>
import ButtonLera from './ui/ButtonLera.vue';
</script>


<template>
    <section class=" bg-[#FCEED5] rounded-bl-[30px] rounded-br-[30px] relative overflow-hidden">
            <div class="max-w-[414px] xl:max-w-[1180px] mx-auto  flex flex-col xl:flex-row ">
            <div class="flex flex-col gap-6 xl:gap-[34px]">
                <div>
                    <div class="hidden  w-[67px] h-[67px] rotate--25_23 rounded-[20px] bg-[#F7DBA7] absolute top-[100px] left-[350px] z-0 "></div>
                    <h1 class="font-extrabold  text-accent xl:text-[60px] text-[46px] relative z-10 mt-[80px]">
                        One more friend
                        <div class="w-[14.63px] h-[14.63px] rounded-[4px] rotation--20_79 bg-[#F7DBA7]  absolute xl:left-[610px] xl:top-[-30px] left-[350px] top-[53px]"></div>
                        <div class="w-[27.5px] h-[27.5px] rounded-[9px] bg-[#F7DBA7] rotate--22_85 absolute xl:left-[600px] xl:top-[10px] z-0 left-[300px] "></div>
                        <div class="w-[21.47px] h-[21.47px] rounded-[6px] rotation--43 bg-accent absolute xl:left-[600px] xl:top-[23px] left-[290px] "></div>
                    </h1>
                    <h2 class="font-bold xl:text-[48px]  text-accent1  text-[28px]">
                        Thousands more fun!
                    </h2>
                </div>
                <p class="text-[12px] text-accent font-medium  xl:text-[16px]">
                    Having a pet means you have more joy, a new friend, a happy <br />
                    person who will always be with you to have fun. We have 200+ <br />
                    different pets that can meet your needs!
                </p>
                <div class="flex  flex-row  gap-[16px] xl:gap-[20px]">
                    <ButtonLera type="border">
                        View Intro
                        <img src="../assets/img/Play_Circle.svg" alt="Play_Circle" />
                    </ButtonLera>

                    <ButtonLera type="fill">
                        Explore Now
                    </ButtonLera>
                </div>
            </div>
            <img src="../assets/img/img-dog.svg" alt="img dog" class="w-[650px] flex relative z-10 ">
            <div class="w-[635px] h-[635px] rounded-[99px] rotate--9_35  absolute bg-accent z-0 xl:left-[865.80px] xl:top-[268px] top-[460px] left-[70px]"></div>
            <div class="w-[635px] h-[635px] rounded-[99px] rotate--25_23  absolute bg-[#F7DBA7] z-3 xl:left-[930.67px] xl:top-[180px] top-[440px] left-[100px]"></div>
      </div>


    </section>
</template>
