<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  color: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  subtitle: {
    type: String,
    required: true
  },
  side: {
    type: String,
    required: true
  }
});
</script>

<template>
    <div class="timecard-box" :style="{backgroundColor: props.color}">
      <span></span>
      <slot></slot>
      <div :class="['text-box', props.side]">
        <h1>{{ props.title }}</h1>
        <h2>{{ props.subtitle }}</h2>
        <p><slot name="text"></slot></p>
      </div>
    </div>
</template>

<style scoped>
  .timecard-box {
    position: relative;

    width: 100%;
    height: 45vh;
    overflow: hidden;
  }

  span {
    display: block;
    width: 30px;
    height: 30px;
    background-color: black;

    position: absolute;
    left: 50%;
    top: 50%;

    transform: translate(-50%, -50%);

    border-radius: 50px;

  }

  .text-box {
    position: absolute;

    display: flex;
    flex-direction: column;

    top: 50%;

    transform: translateY(-50%);

    width: 15vw;
  }

  .right {
    right: 52%;
  }

  .right * {
    text-align: end;
  }

  .left {
    left: 52%;
  }

  h1 {
    font-size: 4rem;

    line-height: normal;

    font-weight: 600;
    margin: 0;
    padding: 0;
  }

  h2 {
    font-size: 2.2rem;

    font-weight: 600;
  }
</style>
