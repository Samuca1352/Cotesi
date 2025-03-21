
<template>
  <div class="bg-white border-gray-200 dark:bg-black flex justify-center dark:text-white pt-10">
    <div class="container">
      <HeaderPage></HeaderPage>
    </div>
  </div>
  <div id="ttudo">

  
  <div id="tudo">
    <div class="pages h-screen panel flex items-center justify-center" style="">


  <calendar-range class="cally bg-base-100 border border-base-300 shadow-lg rounded-box" value="2025-05-08/2025-05-16">
    <svg aria-label="Previous" class="fill-current size-4" slot="previous" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="currentColor" d="M15.75 19.5 8.25 12l7.5-7.5"></path></svg>
    <svg aria-label="Next" class="fill-current size-4" slot="next" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="currentColor" d="m8.25 4.5 7.5 7.5-7.5 7.5"></path></svg>
    <calendar-month></calendar-month>

  </calendar-range>
  <button type="button" id="tes" class="text-white bg-gray-800 hover:bg-gray-900 focus:outline-none focus:ring-4 focus:ring-gray-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:hover:bg-gray-700 dark:focus:ring-gray-700 dark:border-gray-700">Dark</button>

</div>
    <div class="pages lg:flex md:flex">
      <div class="title panel h-screen text-gray-900 text-8xl flex items-center justify-center"
        style="font-family: 'TuskerGrotesk'; width: 50vw; ">
        <div class="test text-wrap">

          O QUE É COTESI?
        </div>
      </div>
      <div class="description panel flex-wrap flex items-center justify-center " style="margin-bottom: 10vh;">
        <div class="p">
          O IX Congresso de Tecnologia e Sistemas de Informação (COTESI) é um evento concebido pelo corpo docente da
          área
          de informática do Câmpus Votuporanga. O COTESI é constituído por palestras e minicursos.
        </div>
        <div class="p mt-10">
          Atualmente a Comissão Organizadora é composta por representantes do corpo docente e discente dos cursos de
          graduação de Sistemas de Informação instituída pela portaria nº. VTP.15/2024, de 21 de fevereiro de 2024.
        </div>
        <div class="p mt-10 ultimo">
          Este evento tem como intuito complementar a formação acadêmica dos alunos e discutir temas atuais da área da
          Tecnologia da Informação relacionados com o Ensino, Pesquisa e Extensão, além de fatos e episódios recentes
          relacionados a aspectos transversais, como Meio Ambiente & Sustentabilidade e Responsabilidade Social. O
          evento
          é gratuito e aberto à comunidade.
        </div>
        <div class="p mt-10 ultimo">
          Este evento tem como intuito complementar a formação acadêmica dos alunos e discutir temas atuais da área da
          Tecnologia da Informação relacionados com o Ensino, Pesquisa e Extensão, além de fatos e episódios recentes
          relacionados a aspectos transversais, como Meio Ambiente & Sustentabilidade e Responsabilidade Social. O
          evento
          é gratuito e aberto à comunidade.
        </div>
        <div class="p mt-10 ultimo">
          Este evento tem como intuito complementar a formação acadêmica dos alunos e discutir temas atuais da área da
          Tecnologia da Informação relacionados com o Ensino, Pesquisa e Extensão, além de fatos e episódios recentes
          relacionados a aspectos transversais, como Meio Ambiente & Sustentabilidade e Responsabilidade Social. O
          evento
          é gratuito e aberto à comunidade.
        </div>
      </div>
    </div>
    <div id="tes" class="black pages h-screen panel flex items-center justify-center" style="background-color: #0176ff; ">
      Mais espaço para simular conteúdo longo
    </div>
  </div>
</div>
</template>
<script setup>
import "cally";

import HeaderPage from './components/HeaderPage.vue';
import { gsap } from "gsap";
import { onMounted } from 'vue';
import { ScrollTrigger } from "gsap/ScrollTrigger";
import Lenis from 'lenis'
gsap.registerPlugin(ScrollTrigger);




onMounted(() => {
  

// Initialize Lenis
const lenis = new Lenis({
  autoRaf: true,
  duration: 2,
  autoResize: true
});

// Listen for the scroll event and log the event data
lenis.on('scroll', (e) => {
  //algum comando ao scroll
});


  let tl = gsap.timeline({
    scrollTrigger: {
        trigger: ".test",
        toggleActions: "resume pause reverse pause", //quando chega nele / quando passa dele / quando passa e volta nele
        start: "top center", //elemento e página ou seja começa quando a parte de cima do elemento atinge o centro da pag
        end: "bottom 50px",
        scrub: 3, //vai junto com a página / pode ser true ou false ou um valor (suaviza mais)
    },
});
//   let gl = gsap.timeline({
//     scrollTrigger: {
//         trigger: ".description",
//         toggleActions: "restart pause reverse pause", //quando chega nele / quando passa dele / quando passa e volta nele
//         start: "top center", //elemento e página ou seja começa quando a parte de cima do elemento atinge o centro da pag
//         end: "bottom bottom",
//         scrub: 3, //vai junto com a página / pode ser true ou false ou um valor (suaviza mais)
//         markers: true, //marcadores
//     },
// });


tl.from('.test', {

x: -100,
duration: 3,
});

// gl.to('.description', {
// y:-230,
// duration: 1,
// });

  const larguraTela = window.innerWidth;



  function verificaTela() {

    if (larguraTela > 768) {
      ScrollTrigger.create({
        trigger: ".title",
        endTrigger: ".description",
        start: "top top",
        end: "bottom 95%",
        pin: true,
        markers: true,

      });
    }



    window.addEventListener('resize', verificaTela);
  }

  verificaTela();




  // ScrollTrigger.create({
  //     trigger: ".pink",
  //     start: "top bottom",
  //     end: "bottom top",
  //     scrub: 1, // Quanto maior, mais suave
  //   });
  // gsap.utils.toArray(".pages").forEach((pages, i)=>{
  //       ScrollTrigger.create({
  //       trigger: pages,
  //       xPercent: -100 * (pages.length -1), // EFEITO CAMADAS
  //       start:"top top",
  //       pinSpacing:false,
  //       pin:true,
  //   })
  //   })
});


</script>

<style>
body {
  overflow-x: hidden;
  background-color: #e2e4e6;
}
.cont {
  display: flex;
}

.bg-base-100 {
    background-color: #151515;
}

.cally {
    ::part(button day today) {
        background: #2f9e41;
        color: var(--color-primary-content);
    }

    
    ::part(range-start) {
        border-start-end-radius: 0;
        border-end-end-radius: 0;
    }

    ::part(range-end) {
        border-start-start-radius: 0;
        border-end-start-radius: 0;
    }
    
}



@media (max-width: 767px) {

  /*celular */
  .description {
    margin-top: -40%;
    padding-top: 15%;
    color: #002b5e;
    font-weight: 400;
    letter-spacing: -.03em;
    line-height: 125%;
    font-size: 4.2666666667vw;

  }
}

@media (min-width: 768px) {

  .description {
    width: 50vw;
    padding-top: 63vh;
    color: #002b5e;
    /* Ajuste para que seja maior que a altura do texto fixo */
  }

}


.test {
  border-left: 4px solid #0176ff;
  padding-left: 5px;
  width: 50%;

  line-height: 120%;
}


.tk {
  background-color: white;
}


.p {
  width: 80%;
  margin-top: 50px;
}

.p:first-child {
  margin-top: 0;
}
</style>
