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
  },
  link: {
    type: String
  }
});
</script>

<template>
    <div :class="['timecard-box', textColor]" :style="{backgroundColor: props.color}">
      <a :href="props.link">
          <div class="link" style="z-index: 50;">
            <h3 style="color: white;">Clique para mais informações</h3>
          </div>
      </a>

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

  .link {
    display: none;
    position: absolute;
    background-color: black;
    color: transparent;
    padding: 7px 10px;
    border-radius: 10px;

    top: -8vh;
    left: 50%;
    transform: translateX(-50%);

    width: max-content;

    font-family: "Glacial";
  }

  a:hover .link {
    display: block;
  }

  a {
    display: block;
    width: 30px;
    height: 30px;
    background-color: black;

    position: absolute;
    left: 50%;
    top: 35%;

    transform: translate(-50%, -50%);

    border: 5px solid black;
    border-radius: 50px;
    z-index: 20;

    transition: 1s all;
    animation: glowing-border 1.5s infinite alternate;
  }

  @keyframes glowing-border {
      0% {
        border-color: black;
      }
      100% {
        border-color: red;
      }
  }

  a:hover {
    cursor: pointer;
    background-color: white;
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
