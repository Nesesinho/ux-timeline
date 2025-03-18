<script setup>
import { onMounted } from "vue";
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


const observer = new IntersectionObserver((entries) => {
  entries.forEach((entry) => {
    if (entry.isIntersecting) {
      entry.target.classList.add("show");
    }
  });
});

onMounted(() => {
  document.querySelectorAll(".fade-in").forEach((el) => observer.observe(el));
});
</script>

<template>
    <div :class="['timecard-box', textColor, 'fade-in']" :style="{backgroundColor: props.color}">
      <span></span>
      <slot></slot>
      <div :class="['text-box', props.side]">
        <div class="title" v-if="props.side === 'left'">
          <h1>
            {{ props.title }}
          </h1>
          <a :href="props.link">
              <div class="link" style="z-index: 100;">
                <h3 style="color: white;">Clique para mais informações</h3>
              </div>
          </a>
        </div>
        <div class="title" style="justify-content: end;" v-else>
          <a :href="props.link">
            <div class="link" style="z-index: 100;">
              <h3 style="color: white;">Clique para mais informações</h3>
            </div>
          </a>
          <h1>
            {{ props.title }}
          </h1>
        </div>
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
    z-index: 1;
  }

  span {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    width: 40px;
    height: 10px;
    top: 16vh;

    border-radius: 5px;

    display: block;
    background-color: black;
  }

  .link {
    display: none;
    position: absolute;
    background-color: black;
    color: transparent;
    padding: 7px 10px;
    border-radius: 10px;

    top: -3vh;
    left: 50%;
    transform: translateX(-50%);

    width: max-content;

    font-family: "Glacial";
  }

  .title {
    display: flex;
    align-items: center;
  }

  a:hover .link {
    display: block;
  }

  a {
    display: block;
    width: 30px;
    height: 30px;
    background-color: black;
    margin: 8px;

    border: 5px solid black;
    border-radius: 50px;

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

  .fade-in {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.6s ease-out, transform 0.6s ease-out;
  }

  .fade-in.show {
    opacity: 1;
    transform: translateY(0);
  }
</style>
