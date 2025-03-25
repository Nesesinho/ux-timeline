<script setup>
import TimeCard from "/src/components/TimeCard.vue"
import TimeLine from "/src/components/TimeLine.vue"
import PropImage from "/src/components/PropImage.vue"
</script>

<template>
  <main>
    <TimeCard side="left" color="#545454" title="1999" subtitle="MEMEX" link="https://www.tecmundo.com.br/historia/9528-a-historia-da-interface-grafica.htm">
      <template #text>Vannevar Bush propõe o Memex, um sistema de organização e recuperação de informações, precursor da hipertextualidade.</template>
      <PropImage src="/imgs/1945/background.png" width="130%" top="-100" left="-2"/>
      <PropImage src="/imgs/1945/man.png" height="100%" bottom="0" left="15"/>
      <PropImage src="/imgs/1945/furniture.png" right="0" height="85%" bottom="5"/>
    </TimeCard>
    <TimeCard side="right" color="#737373" title="1950" subtitle="TESTE DE TURING" link="https://www.inthepocket.com/blog/what-alan-turing-can-teach-us-about-ux">
      <template #text>Alan Turing introduz o Teste de Turing, questionando a capacidade das máquinas de interagir como humanos.</template>
      <PropImage src="/imgs/1950/background.png" width="150%" top="-30" left="-20"/>
      <PropImage src="/imgs/1950/man.png" height="100%" bottom="0" right="0"/>
      <PropImage src="/imgs/1950/furniture.png" left="5" height="100%" bottom="0"/>
    </TimeCard>
    <TimeCard side="left" color="#d9d9d9" title="1963" subtitle="Sketchpad" textColor="black" link="https://www.tecmundo.com.br/historia/9528-a-historia-da-interface-grafica.htm">
      <template #text>Ivan Sutherland desenvolve o Sketchpad, uma interface gráfica pioneira.</template>
      <PropImage src="/imgs/1963/background.png" width="80%" top="-20" right="5"/>
      <PropImage src="/imgs/1963/picture.png" height="100%" bottom="0" right="-8"/>
      <PropImage src="/imgs/1963/man.png" height="100%" bottom="0"/>
    </TimeCard>
    <TimeCard side="right" color="#fafafa" title="1969" subtitle="The Mother of All Demos" textColor="black" link="https://www.tecmundo.com.br/historia/9528-a-historia-da-interface-grafica.htm">
      <template #text>Douglas Engelbart apresenta The Mother of All Demos, demonstrando o mouse, hipertexto e interfaces gráficas.</template>
      <PropImage src="/imgs/1969/background.png" width="100%" top="-20" right="5"/>
      <PropImage src="/imgs/1969/man2.png" height="100%" bottom="0" right="-2"/>
      <PropImage src="/imgs/1969/man.png" height="110%" bottom="0" left="5"/>
      <PropImage src="/imgs/1969/furniture.png" height="70%" bottom="0"/>
    </TimeCard>
    <TimeCard side="left" color="#ffe689" title="1973" subtitle="Xerox Alto" textColor="black" link="https://www.tecmundo.com.br/historia/9528-a-historia-da-interface-grafica.htm">
      <template #text> O Xerox Alto é lançado, trazendo um sistema operacional com interface gráfica baseada em janelas.</template>
      <PropImage src="/imgs/1973/background.png" width="90%" top="0" right="2"/>
      <PropImage src="/imgs/1973/furniture2.png" height="100%" bottom="0" right="-4"/>
      <PropImage src="/imgs/1973/man.png" height="100%" bottom="0" left="17"/>
      <PropImage src="/imgs/1973/furniture.png" height="110%" bottom="0" left="-8"/>
    </TimeCard>
    <TimeCard side="right" color="#f9b566" title="1984" subtitle="Macintosh" textColor="black" link="https://www.tecmundo.com.br/historia/9528-a-historia-da-interface-grafica.htm">
      <template #text>  A Apple lança o Macintosh, popularizando a interface gráfica e o conceito de usabilidade amigável.</template>
      <PropImage src="/imgs/1984/prop.png" width="25%" top="10" left="10"/>
      <PropImage src="/imgs/1984/prop2.png" height="100%" bottom="0" right="-2"/>
      <PropImage src="/imgs/1984/furniture.png" height="120%" bottom="-25" left="-5"/>
      <PropImage src="/imgs/1984/furniture2.png" height="80%" bottom="4" right="0"/>
    </TimeCard>
    <TimeCard side="left" color="#e76144" title="1991" subtitle="HTML Tags </>" textColor="black" link="https://www.webdesignmuseum.org/web-design-history/tim-berners-lee-published-a-document-called-html-tags-1991">
      <template #text>Publicado o documento HTML Tags, estabelecendo a base da web.</template>
      <PropImage src="/imgs/1991/prop3.png" height="35%" bottom="3" right="1"/>
      <PropImage src="/imgs/1991/prop.png" height="100%" top="-8" left="-8"/>
      <PropImage src="/imgs/1991/prop2.png" height="90%" bottom="22" right="-10"/>
      <PropImage src="/imgs/1991/prop4.png" height="40%" bottom="4" left="2"/>
    </TimeCard>
    <TimeCard side="right" color="#cb2222" title="1992" subtitle="Primeira foto" textColor="black" link="https://www.telegraph.co.uk/technology/news/9391110/How-the-first-photo-was-posted-on-the-Web-20-years-ago.html">
      <template #text> Publicada a primeira foto na Web das Les Horribles Cernettes, banda fundada por funcionárias do CERN (Organização Europeia para Pesquisa Nuclear).</template>
      <PropImage src="/imgs/1992/background.png" height="100%" top="0" right="-5"/>
      <PropImage src="/imgs/1992/womans.png" height="112%" bottom="0" right="-1"/>
      <PropImage src="/imgs/1992/prop.png" height="160%" top="-32" left="-18"/>
    </TimeCard>
    <TimeCard side="left" color="#ff5757" title="1993" subtitle="MOSAIC" textColor="black" link="https://alternativapara.com.br/blog/a-revolucao-do-mosaic-o-navegador-que-mudou-a-historia-da-web">
      <template #text>
        Surge o Mosaic, o primeiro navegador gráfico, trazendo ícones e imagens para a web.
        <h1>Primeira versão do HTML.</h1>
      </template>
      <PropImage src="/imgs/1993/prop2.png" height="65%" bottom="30" left="20"/>
      <PropImage src="/imgs/1993/prop.png" height="100%" top="0" left="0"/>
      <PropImage src="/imgs/1993/prop4.png" height="90%" bottom="4" right="-18"/>
      <PropImage src="/imgs/1993/prop3.png" height="70%" top="4" right="-1"/>
    </TimeCard>
    <TimeCard side="right" color="#ff9292" title="1994" subtitle="Netscape Navigator" textColor="black" link="https://museucapixaba.com.br/hoje/hypertext-markup-language-html-de-1993/">
      <template #text>O Netscape Navigator introduz menus, botões e barras de rolagem, melhorando a experiência do usuário.</template>
      <PropImage src="/imgs/1994/prop2.png" height="90%" bottom="5" left="2"/>
      <PropImage src="/imgs/1994/prop.png" height="95%" top="2" right="1"/>
      <PropImage src="/imgs/1994/animals.png" height="50%" bottom="2" right="-5"/>
      <PropImage src="/imgs/1994/animals2.png" height="90%" bottom="-6" left="-3"/>
    </TimeCard>
    <TimeCard side="left" color="#ffabd3" title="1995" subtitle="Donald Norman" textColor="black" link="https://pt.wikipedia.org/wiki/Netscape_Navigator">
      <template #text>Donald Norman cunha oficialmente o termo User Experience (UX) enquanto trabalhava na Apple.</template>
      <PropImage src="/imgs/1995/background.png" width="110%" top="-15" left="-9"/>
      <PropImage src="/imgs/1995/man.png" height="100%" bottom="0" right="0"/>
      <PropImage src="/imgs/1995/prop.png" height="95%" bottom="-13" left="-5"/>
      <PropImage src="/imgs/1995/prop2.png" height="95%" bottom="0" left="38"/>
    </TimeCard>
    <TimeCard side="right" color="#ff92dd" title="1996" subtitle="heurísticas" textColor="black" link="https://www.mergo.com.br/blog/user-experience/don-norman-principios-design/">
      <template #text>Jakob Nielsen publica as heurísticas de usabilidade, influenciando o design web.</template>
      <template #moresubtitle>CSS</template>
      <template #moretext>Criado o CSS (Cascading Style Sheets) por Håkon Wium Lie, permitindo separar o design da estrutura HTML.</template>

      <PropImage src="/imgs/1996/background.png" width="115%" bottom="-5" left="-9"/>
      <PropImage src="/imgs/1996/man.png" height="110%" bottom="0" right="-10"/>
      <PropImage src="/imgs/1996/man2.png" height="135%" bottom="-13" left="-5"/>
    </TimeCard>
    <TimeCard side="left" color="#c263bf" title="1999" subtitle="WEB 2.0" link="https://pt.wikipedia.org/wiki/Jakob_Nielsen">
      <template #text>O conceito de Web 2.0 emerge, trazendo sites mais interativos e sociais.</template>
      <PropImage src="/imgs/1999/prop2.png" height="100%" bottom="0" right="-13"/>
      <PropImage src="/imgs/1999/prop.png" height="55%" bottom="0" right="-4"/>
      <PropImage src="/imgs/1999/prop3.png" height="115%" bottom="-10" left="2"/>
      <PropImage src="/imgs/1999/prop4.png" height="80%" bottom="9" left="18"/>
    </TimeCard>
    <TimeCard side="right" color="#5f3ba7" title="2003" subtitle="WORDPRESS" link="">
      <template #text> Surge o WordPress, facilitando a criação de sites com templates customizáveis..</template>
      <PropImage src="/imgs/2003/prop2.png" height="100%" bottom="0" left="29"/>
      <PropImage src="/imgs/2003/prop.png" height="120%" bottom="0" right="0"/>
      <PropImage src="/imgs/2003/prop3.png" height="25%" top="2.1" left=".6"/>
      <PropImage src="/imgs/2003/prop4.png" height="100%" bottom="0" right="0"/>
    </TimeCard>
    <TimeCard side="left" color="#3a4695" title="2004" subtitle="FACEBOOK" link="">
      <template #text>O Facebook é lançado, redefinindo a experiência do usuário com interfaces sociais.</template>
      <PropImage src="/imgs/2004/prop.png" height="80%" bottom="0" left="12"/>
    </TimeCard>
    <TimeCard side="right" color="#244fa2" title="2007" subtitle="IPHONE" link="">
      <template #text> O iPhone revolucionou o UX mobile, tornando o design responsivo essencial.</template>
      <PropImage src="/imgs/2007/prop3.png" height="110%" bottom="-7" left="1"/>
      <PropImage src="/imgs/2007/prop4.png" height="105%" bottom="-2.5" right="1"/>
      <PropImage src="/imgs/2007/prop.png" height="60%" bottom="0" left="4"/>
      <PropImage src="/imgs/2007/prop2.png" height="90%" top="4" right="5"/>
    </TimeCard>
    <TimeCard side="left" color="#4078c2" title="2008" subtitle="HTML 5" link="">
      <template #text>Surge o HTML5, trazendo suporte nativo a vídeos, áudio e elementos semânticos</template>
      <PropImage src="/imgs/2008/prop.png" height="90%" bottom="0" right="-10"/>
      <PropImage src="/imgs/2008/prop2.png" height="98%" top="0" left="0"/>
      <PropImage src="/imgs/2008/man.png" height="110%" bottom="0" left="3"/>
    </TimeCard>
    <TimeCard side="right" color="#42969c" title="2014" subtitle="MATERIAL DESIGN" link="">
      <template #text>O Google lança o Material Design, criando diretrizes visuais para aplicativos e sites.</template>
      <PropImage src="/imgs/2014/prop.png" height="90%" bottom="0" left="0"/>
      <PropImage src="/imgs/2014/prop2.png" height="60%" top="15" left="10"/>
      <PropImage src="/imgs/2014/prop3.png" height="100%" top="0" right="2"/>
      <PropImage src="/imgs/2014/prop4.png" height="70%" top="12" right="10"/>
    </TimeCard>
    <TimeCard side="left" color="#469071" title="2023" subtitle="IA GENERATIVA" link="">
      <template #text>IA Generativa impacta o UX na web com personalização automatizada.</template>
      <PropImage src="/imgs/2023/prop.png" height="190%" top="-95" left="-1"/>
      <PropImage src="/imgs/2023/prop2.png" height="120%" top="-20" right="-10"/>
    </TimeCard>
    <TimeCard side="right" color="#19793c" title="2024" subtitle="IA APLICADA AO UX" link="">
      <template #text> IA aplicada ao UX continua evoluindo..</template>
      <PropImage src="/imgs/2024/prop.png" height="130%" top="-20" left="-15"/>
      <PropImage src="/imgs/2024/prop2.png" height="100%" top="0" right="20"/>
      <PropImage src="/imgs/2024/prop3.png" height="130%" top="0" right="-10"/>
      <PropImage src="/imgs/2024/prop4.png" height="50%" top="28" left="5"/>
    </TimeCard>´
    <TimeLine />
  </main>
</template>

<style scoped>
  main {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    gap: 3vh;

    width: 100%;
    min-height: 100vh;
    height: fit-content;

    overflow-y: hidden;
    overflow-x: hidden;
  }

  main::-webkit-scrollbar {
    display: none;
  }

</style>
