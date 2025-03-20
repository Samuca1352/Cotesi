<template>
    <div class="bg-white border-gray-200 dark:bg-black flex justify-center dark:text-white pt-10">
      <div class="container">
        <HeaderPage></HeaderPage>
      </div>
    </div>
    <div class="pages h-screen panel flex items-center justify-center" style="">
    Mais espaço para simular conteúdo longo
  </div>
    <div class="tk lg:flex md:flex">
      <div class="blue panel h-screen text-gray-900 text-8xl flex items-center justify-center" style="font-family: 'TuskerGrotesk'; width: 50vw; ">
        <div class="test text-wrap">
  
          O QUE É COTESI?
        </div>
      </div>
      <div class="pink panel flex-wrap flex items-center justify-center "  style="margin-bottom: 10vh;">
        <div class="p">
          O IX Congresso de Tecnologia e Sistemas de Informação (COTESI) é um evento concebido pelo corpo docente da área de informática do Câmpus Votuporanga. O COTESI é constituído por palestras e minicursos.
        </div>
        <div class="p mt-10">
          Atualmente a Comissão Organizadora é composta por representantes do corpo docente e discente dos cursos de graduação de Sistemas de Informação instituída pela portaria nº. VTP.15/2024, de 21 de fevereiro de 2024.
        </div>
        <div class="p mt-10 ultimo">
          Este evento tem como intuito complementar a formação acadêmica dos alunos e discutir temas atuais da área da Tecnologia da Informação relacionados com o Ensino, Pesquisa e Extensão, além de fatos e episódios recentes relacionados a aspectos transversais, como Meio Ambiente & Sustentabilidade e Responsabilidade Social. O evento é gratuito e aberto à comunidade.
        </div>
      </div>
    </div>
    <div class="black h-screen panel flex items-center justify-center" style="background-color: #0176ff; ">
      Mais espaço para simular conteúdo longo
    </div>
  </template>
  <script setup>
  import HeaderPage from './components/HeaderPage.vue';
  import { gsap } from "gsap";
  import { onMounted } from 'vue';
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  gsap.registerPlugin(ScrollTrigger);
  
  
  
  onMounted(() => {
  
    const larguraTela = window.innerWidth;
  
  
    
    function verificaTela(){
      
      if(larguraTela> 768){
        ScrollTrigger.create({
          trigger: ".blue",
          start: "top top",
          end: "bottom center",
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
  
  @media (max-width: 767px) { /*celular */
    .pink {
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
  
    .pink {
      width: 50vw;
      padding-top: 63vh; /* Ajuste para que seja maior que a altura do texto fixo */
    }
  
  }
  
  
  .test {
    border-left: 4px solid  #0176ff;
    padding-left: 5px;
    width: 50%;
   
    line-height: 120%;
  }
  
  
  .tk{
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
  