<script setup>
import TimeCard from "/src/components/TimeCard.vue"
import TimeLine from "/src/components/TimeLine.vue"
</script>

<template>
  <main>
    <TimeLine />
    <TimeCard side="left" color="#545454" title="1999" subtitle="MEMEX">
      <template #text>algum texto muito comprido pois preciso textar esse texto</template>
    </TimeCard>
  </main>
</template>

<style scoped>
  main {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    gap: 3vh;

    width: 80%;
    min-height: 100vh;
    height: fit-content;

    overflow-y: visible;
    overflow-x: hidden;
  }
</style>
