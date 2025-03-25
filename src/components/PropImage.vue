<script setup>
import { computed, ref } from 'vue';

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
  position: 'absolute'
}));
</script>

<template>
  <img ref="image" :src="backgroundImage" :alt="alt" :style="style" :class="align">
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
</style>
