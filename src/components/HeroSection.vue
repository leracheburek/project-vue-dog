<script setup>
import ButtonLera from './ui/ButtonLera.vue';
import WithComponent from './ui/WithComponent.vue';
</script>


<template>
    <section class="bg-[#FCEED5] rounded-bl-[30px] rounded-br-[30px] pb-[130px]">
        <WithComponent>

            <div class=" flex flex-col gap-6 xl:gap-[34px]">
                <div>
                    <h1 class="font-extrabold text-10  text-accent xl:text-[60px] sm:text-10 ">
                        One more friend
                    </h1>
                    <h2 class="font-bold xl:text-[48px]  text-accent  mb:text-[25px]">
                        Thousands more fun!
                    </h2>
                </div>

                <p class="text-[12px] text-accenе font-medium  xl:text-[16px]">
                    Having a pet means you have more joy, a new friend, a happy <br />
                    person who will always be with you to have fun. We have 200+ <br />
                    different pets that can meet your needs!
                </p>

                <div class="flex  flex-row items-center  gap-1 sm:items-start sm:gap-5">
                    <ButtonLera type="border">
                        View Intro
                        <img src="../assets/img/Play_Circle.svg" alt="Play_Circle" />
                    </ButtonLera>


                    <ButtonLera type="fill">
                        Explore Now
                    </ButtonLera>

                </div>
            </div>

            <img src="../assets/img/img-dog.svg" alt="img dog" class="xl:w-[414px] h-[386px]">

        </WithComponent>

    </section>
</template>
