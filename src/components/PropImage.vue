<script setup>
import { computed, ref, onMounted } from 'vue';

const image = ref("null");
const aspectRatio = ref("auto");

const calcAspectRatio = () => {
  if (image.value) {
    const largura = image.value.naturalWidth;
    const altura = image.value.naturalHeight;
    aspectRatio.value = `${largura}/${altura}`
  }
};

const props = defineProps({
  src: { type: String, required: true },
  top: { type: String },
  bottom: { type: String },
  left: { type: String },
  right: { type: String },
  width: { type: String },
  height: { type: String },
  alt: { type: String, default: '' },
  align: { type:String }
});

const imagePath = props.src;
const backgroundImage = new URL(imagePath, import.meta.url).href;

const style = computed(() => ({
  top: props.top ? `${props.top}%` : undefined,
  bottom: props.bottom ? `${props.bottom}%` : undefined,
  left: props.left ? `${props.left}%` : undefined,
  right: props.right ? `${props.right}%` : undefined,
  width: props.width ? `${props.width}` : undefined,
  height: props.height ? `${props.height}` : undefined,
  aspectRatio: calcAspectRatio(),
  position: 'absolute',
  TransitionDuration: `${Math.floor(Math.random() * 3) + 1}s`
}));

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
  <img ref="image" :src="backgroundImage" :alt="alt" :style="style" :class="[align, 'fade-in']">
</template>


<style scoped>
  img {
    position: absolute;
  }

  .center-x {
    left: 50%;
    transform: translateX(-50%);
  }

  .center-y {
    top: 50%;
    transform: translateY(-50%);
  }

  .fade-in {
    opacity: 0;
    transform: translateY(-40px);
    transition: opacity ease-out, transform ease-out;
  }

  .fade-in.show {
    opacity: 1;
    transform: translateY(0);
  }
</style>
