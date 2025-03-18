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
  },
  textColor: {
    type: String
  }
});
</script>

<template>
    <div :class="['timecard-box', textColor]" :style="{backgroundColor: props.color}">
      <span></span>
      <slot></slot>
      <div :class="['text-box', props.side]">
        <h1>{{ props.title }}</h1>
        <div class="subtitle">
          <h2>{{ props.subtitle }}</h2>
          <p><slot name="text"></slot></p>
          <div class="moresub">
            <h2 style="text-align: start"><slot name="moresubtitle"></slot></h2>
            <p style="text-align: start"><slot name="moretext"></slot></p>
          </div>
        </div>
      </div>
    </div>
</template>

<style scoped>
  .black * {
    color: black;
  }

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
    top: 35%;

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

  .subtitle {
    position: relative;
    overflow-x: visible;
  }

  .moresub {
    position: absolute;
    top: 0;
    left:120%;
    width: 10vw;
  }
</style>
