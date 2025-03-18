<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  src: {
    type: String,
    required: true
  }
});
</script>

<template>
  <img :src="props.src" alt="">
</template>

<style scoped>
  img {
    position: absolute;
  }
</style>
