<script setup>
import TimeCard from "/src/components/TimeCard.vue"
import TimeLine from "/src/components/TimeLine.vue"
import PropImage from "/src/components/PropImage.vue"
</script>

<template>
  <main>
    <TimeLine />
    <TimeCard side="left" color="#545454" title="1999" subtitle="MEMEX">
      <template #text>algum texto muito comprido pois preciso textar esse texto</template>
      <PropImage src="/src/assets/imgs/1945/background.png" width="130%" top="-100" left="-2"/>
      <PropImage src="/src/assets/imgs/1945/man.png" height="100%" bottom="0" left="15"/>
      <PropImage src="/src/assets/imgs/1945/furniture.png" right="0" height="85%" bottom="5"/>
    </TimeCard>
    <TimeCard side="right" color="#737373" title="1950" subtitle="TESTE DE TURING">
      <template #text>Alan Turing introduz o Teste de Turing, questionando a capacidade das máquinas de interagir como humanos.</template>
      <PropImage src="/src/assets/imgs/1950/background.png" width="150%" top="-30" left="-20"/>
      <PropImage src="/src/assets/imgs/1950/man.png" height="100%" bottom="0" right="0"/>
      <PropImage src="/src/assets/imgs/1950/furniture.png" left="5" height="100%" bottom="0"/>
    </TimeCard>
    <TimeCard side="left" color="#d9d9d9" title="1963" subtitle="Sketchpad">
      <template #text>Ivan Sutherland desenvolve o Sketchpad, uma interface gráfica pioneira.</template>
      <PropImage src="/src/assets/imgs/1963/background.png" width="80%" top="-20" right="5"/>
      <PropImage src="/src/assets/imgs/1963/picture.png" height="100%" bottom="0" right="-8"/>
      <PropImage src="/src/assets/imgs/1963/man.png" height="100%" bottom="0"/>
    </TimeCard>
    <TimeCard side="right" color="#fafafa" title="1969" subtitle="The Mother of All Demos">
      <template #text>Douglas Engelbart apresenta The Mother of All Demos, demonstrando o mouse, hipertexto e interfaces gráficas.</template>
      <PropImage src="/src/assets/imgs/1969/background.png" width="100%" top="-20" right="5"/>
      <PropImage src="/src/assets/imgs/1969/man2.png" height="100%" bottom="0" right="-2"/>
      <PropImage src="/src/assets/imgs/1969/man.png" height="110%" bottom="0" left="5"/>
      <PropImage src="/src/assets/imgs/1969/furniture.png" height="70%" bottom="0"/>
    </TimeCard>
    <TimeCard side="left" color="#ffe689" title="1973" subtitle="Xerox Alto">
      <template #text> O Xerox Alto é lançado, trazendo um sistema operacional com interface gráfica baseada em janelas.</template>
      <PropImage src="/src/assets/imgs/1973/background.png" width="90%" top="0" right="2"/>
      <PropImage src="/src/assets/imgs/1973/furniture2.png" height="100%" bottom="0" right="-4"/>
      <PropImage src="/src/assets/imgs/1973/man.png" height="100%" bottom="0" left="14"/>
      <PropImage src="/src/assets/imgs/1973/furniture.png" height="110%" bottom="0" left="-8"/>
    </TimeCard>
    <TimeCard side="left" color="#ffe689" title="1984" subtitle="Macintosh">
      <template #text>  A Apple lança o Macintosh, popularizando a interface gráfica e o conceito de usabilidade amigável.</template>
      <PropImage src="/src/assets/imgs/1973/background.png" width="90%" top="0" right="2"/>
      <PropImage src="/src/assets/imgs/1973/furniture2.png" height="100%" bottom="0" right="-4"/>
      <PropImage src="/src/assets/imgs/1973/man.png" height="100%" bottom="0" left="14"/>
      <PropImage src="/src/assets/imgs/1973/furniture.png" height="110%" bottom="0" left="-8"/>
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
