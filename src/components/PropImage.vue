<script setup>
import { computed } from 'vue';

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

const style = computed(() => ({
  top: props.top ? `${props.top}%` : undefined,
  bottom: props.bottom ? `${props.bottom}%` : undefined,
  left: props.left ? `${props.left}%` : undefined,
  right: props.right ? `${props.right}%` : undefined,
  width: props.width ? `${props.width}` : undefined,
  height: props.height ? `${props.height}` : undefined,
  position: 'absolute'
}));
</script>

<template>
  <img :src="props.src" :alt="alt" :style="style" :class="align">
</template>


<style scoped>
  img {
    position: absolute;
  }

  .center-x {
    left: 50%;
    transform: translateX(-50%);
  }
</style>
