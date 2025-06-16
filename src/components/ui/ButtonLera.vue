<template>
  <button :class="[
    'w-[161px] h-[48px] text-4 font-medium rounded-[57px]',
    type === 'fill'
      ? 'bg-accent text-white'
      : type === 'border'
        ? 'border-[1.5px] flex gap-2 justify-center items-center text-accent'
        : ''
  ]">
    <slot></slot>
  </button>
</template>

<script setup>
defineProps({
  type: {
    type: String,
  }
});
</script>









   