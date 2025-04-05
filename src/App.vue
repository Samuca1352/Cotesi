<template>
  <div class=" border-gray-200  flex justify-center  pt-3">
    <div class="container">
      <HeaderPage></HeaderPage>
    </div>
  </div>
  <div id="ttudo">


    <div id="tudo">
      <div class="pages h-screen panel flex items-center justify-center">

        <img src="./img/logo.png" alt="">


      </div>

      <div id="tesxc" class="black pages h-screen panel flex items-center justify-center"
        style="background-color: #0176ff; ">
        Mais espaço para simular conteúdo longo
      </div>
      <SobreNos></SobreNos>
      <div id="pcalendar" class="pages h-auto min-h-screen p-15 panel flex items-center justify-center">

        <CalendarDate id="calendar"></CalendarDate>


                      <!-- <p>Selected range: {{ selected }}</p>
                <calendar-range id="calendar" v-model.lazy="selected" class="cally bg-base-100 border border-base-300 shadow-lg rounded-box" value="2025-05-08/2025-05-16">
                  <svg aria-label="Previous" class="fill-current size-4" slot="previous" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="currentColor" d="M15.75 19.5 8.25 12l7.5-7.5"></path></svg>
                  <svg aria-label="Next" class="fill-current size-4" slot="next" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill="currentColor" d="m8.25 4.5 7.5 7.5-7.5 7.5"></path></svg>
                  <calendar-month value="2025-04-08/2025-05-16"></calendar-month>

                </calendar-range> -->


      </div>
<div class="p-14"><PatrocinadoresVue></PatrocinadoresVue></div>
      
    </div>
  </div>
</template>
<script setup>

import HeaderPage from './components/HeaderPage.vue';
import { gsap } from "gsap";
import { onMounted } from 'vue';
import { ScrollTrigger } from "gsap/ScrollTrigger";
import Lenis from 'lenis'
import CalendarDate from "./components/CalendarDate.vue";
import SobreNos from "./components/SobreNos.vue";
import PatrocinadoresVue from "./components/PatrocinadoresVue.vue";
gsap.registerPlugin(ScrollTrigger);


const selected = "2025-05-08/2025-05-16"


onMounted(() => {

  const larguraTela = screen.width;


  // Initialize Lenis
  const lenis = new Lenis({
    autoRaf: true,
    duration: 1.2,
    autoResize: true
  });


  // Synchronize Lenis scrolling with GSAP's ScrollTrigger plugin
  lenis.on('scroll', ScrollTrigger.update);

  //lenis.scrollTo("#calendar")
  function gsapcalendar() {


    if (verificaTela()) {

      let tl = gsap.timeline({
        scrollTrigger: {
          trigger: "#pcalendar",
          toggleActions: "resume pause reverse pause", //quando chega nele / quando passa dele / quando passa e volta nele
          start: "top center", //elemento e página ou seja começa quando a parte de cima do elemento atinge o centro da pag
          end: "top center",
          scrub: 3, //vai junto com a página / pode ser true ou false ou um valor (suaviza mais)
          markers: true,
        },
      });


      tl.from('#pcalendar', {

        x: 600,
        rotation: 50
      })
    }
  }



  function verificaTela() {
    const larguraTela = window.innerWidth;

    if (larguraTela > 768) {
      return true;
    }

    return false

  }

  window.addEventListener('resize', gsapcalendar);


  gsapcalendar()



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
