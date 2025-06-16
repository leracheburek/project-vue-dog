<script setup>
import ButtonLera from './ui/ButtonLera.vue';
</script>

<template>
  <section
    class="max-w-[414px] xl:max-w-[1180px]  m-auto mt-[60px]   ">
    <div class=" bg-[#FCEED5] flex  xl:justify-around  rounded-[20px] pt-[64px]">
      <div>
        <img src="../assets/img/horizontal-shot-adult-girl.svg" alt="horizontal-shot-adult-girl">
      </div>
      <div>
        <h1 class="xl:text-[52px] text-[54px] font-extrabold text-accent text-center xl:text-end ">One more friend</h1>
        <h3 class="xl:text-[36px] text-[24px] font-bold text-accent2 not-even xl:text-end  text-center">Thousands more fun!</h3>
        <p class="text-[12px] leading-[18px] text-accent2  xl:text-end  text-center">Having a pet means you have more
          joy, a new friend, a happy person<br />who will always be with you to have fun. We have 200+ different
          pets<br /> that can meet your needs!</p>
        <div class="flex gap-[20px] font-medium relative xl:left-[80px] pt-[24px]">
          <ButtonLera type="border">
            View Intro
            <img src="../assets/img/Play_Circle.svg" alt="Play_Circle" />
          </ButtonLera>
          <ButtonLera type="fill">
            Explore Now
          </ButtonLera>
        </div>
      </div>
    </div>
  </section>
</template>