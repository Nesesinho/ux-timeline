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
    <TimeCard side="right" color="#f9b566" title="1984" subtitle="Macintosh">
      <template #text>  A Apple lança o Macintosh, popularizando a interface gráfica e o conceito de usabilidade amigável.</template>
      <PropImage src="/src/assets/imgs/1984/prop.png" width="25%" top="10" left="10"/>
      <PropImage src="/src/assets/imgs/1984/prop2.png" height="100%" bottom="0" right="-2"/>
      <PropImage src="/src/assets/imgs/1984/furniture.png" height="120%" bottom="-25" left="-5"/>
      <PropImage src="/src/assets/imgs/1984/furniture2.png" height="80%" bottom="4" right="0"/>
    </TimeCard>
    <TimeCard side="left" color="#e76144" title="1991" subtitle="HTML Tags </>">
      <template #text>Publicado o documento HTML Tags, estabelecendo a base da web.</template>
      <PropImage src="/src/assets/imgs/1991/prop3.png" height="35%" bottom="3" right="1"/>
      <PropImage src="/src/assets/imgs/1991/prop.png" height="100%" top="-8" left="-8"/>
      <PropImage src="/src/assets/imgs/1991/prop2.png" height="90%" bottom="22" right="-10"/>
      <PropImage src="/src/assets/imgs/1991/prop4.png" height="40%" bottom="4" left="2"/>
    </TimeCard>
    <TimeCard side="right" color="#cb2222" title="1992" subtitle="Primeira foto">
      <template #text> Publicada a primeira foto na Web das Les Horribles Cernettes, banda fundada por funcionárias do CERN (Organização Europeia para Pesquisa Nuclear).</template>
      <PropImage src="/src/assets/imgs/1992/background.png" height="100%" top="0" right="-5"/>
      <PropImage src="/src/assets/imgs/1992/womans.png" height="112%" bottom="0" right="-1"/>
      <PropImage src="/src/assets/imgs/1992/prop.png" height="160%" top="-32" left="-18"/>
    </TimeCard>
    <TimeCard side="left" color="#ff5757" title="1993" subtitle="MOSAIC">
      <template #text>
        Surge o Mosaic, o primeiro navegador gráfico, trazendo ícones e imagens para a web.
        <h1>Primeira versão do HTML.</h1>
      </template>
      <PropImage src="/src/assets/imgs/1993/prop2.png" height="65%" bottom="30" left="20"/>
      <PropImage src="/src/assets/imgs/1993/prop.png" height="100%" top="0" left="0"/>
      <PropImage src="/src/assets/imgs/1993/prop4.png" height="90%" bottom="4" right="-18"/>
      <PropImage src="/src/assets/imgs/1993/prop3.png" height="70%" top="4" right="-1"/>
    </TimeCard>
    <TimeCard side="right" color="#ff9292" title="1994" subtitle="Netscape Navigator">
      <template #text>O Netscape Navigator introduz menus, botões e barras de rolagem, melhorando a experiência do usuário.</template>
      <PropImage src="/src/assets/imgs/1994/prop2.png" height="90%" bottom="5" left="2"/>
      <PropImage src="/src/assets/imgs/1994/prop.png" height="95%" align="center-y" right="1"/>
      <PropImage src="/src/assets/imgs/1994/animals.png" height="50%" bottom="2" right="-5"/>
      <PropImage src="/src/assets/imgs/1994/animals2.png" height="90%" bottom="-6" left="-3"/>
    </TimeCard>
    <TimeCard side="left" color="#ffabd3" title="1995" subtitle="Donald Norman">
      <template #text>Donald Norman cunha oficialmente o termo User Experience (UX) enquanto trabalhava na Apple.</template>
      <PropImage src="/src/assets/imgs/1995/background.png" width="110%" top="-15" left="-9"/>
      <PropImage src="/src/assets/imgs/1995/man.png" height="100%" bottom="0" right="0"/>
      <PropImage src="/src/assets/imgs/1995/prop.png" height="95%" bottom="-13" left="-5"/>
      <PropImage src="/src/assets/imgs/1995/prop2.png" height="95%" bottom="0" left="38"/>
    </TimeCard>
    <TimeCard side="right" color="#ff92dd" title="1996" subtitle="heurísticas">
      <template #text>Jakob Nielsen publica as heurísticas de usabilidade, influenciando o design web.</template>
      <PropImage src="/src/assets/imgs/1996/background.png" width="115%" bottom="-5" left="-9"/>
      <PropImage src="/src/assets/imgs/1996/man.png" height="110%" bottom="0" right="-10"/>
      <PropImage src="/src/assets/imgs/1996/man2.png" height="135%" bottom="-13" left="-5"/>
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
