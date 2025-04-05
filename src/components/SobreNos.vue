<template>
    <div class="pages pagetitle lg:flex md:flex">
        <div class="title panel h-screen text-gray-900 text-8xl flex items-center justify-center"
            style="font-family: 'TuskerGrotesk'; width: 50vw; ">
            <div id="title" class="test text-wrap">

                O QUE É COTESI?
            </div>
        </div>

        <div class="description panel flex-wrap flex items-center justify-center " style="margin-bottom: 10vh;">
            <div class="p">
                O IX Congresso de Tecnologia e Sistemas de Informação (COTESI) é um evento concebido pelo corpo docente
                da
                área
                de informática do Câmpus Votuporanga. O COTESI é constituído por palestras e minicursos.
            </div>
            <div class="p mt-10">
                Atualmente a Comissão Organizadora é composta por representantes do corpo docente e discente dos cursos
                de
                graduação de Sistemas de Informação instituída pela portaria nº. VTP.15/2024, de 21 de fevereiro de
                2024.
            </div>
            <div class="p mt-10 ultimo">
                Este evento tem como intuito complementar a formação acadêmica dos alunos e discutir temas atuais da
                área da
                Tecnologia da Informação relacionados com o Ensino, Pesquisa e Extensão, além de fatos e episódios
                recentes
                relacionados a aspectos transversais, como Meio Ambiente & Sustentabilidade e Responsabilidade Social. O
                evento
                é gratuito e aberto à comunidade.
            </div>
            <div class="p mt-10 ultimo">
                Este evento tem como intuito complementar a formação acadêmica dos alunos e discutir temas atuais da
                área da
                Tecnologia da Informação relacionados com o Ensino, Pesquisa e Extensão, além de fatos e episódios
                recentes
                relacionados a aspectos transversais, como Meio Ambiente & Sustentabilidade e Responsabilidade Social. O
                evento
                é gratuito e aberto à comunidade.
            </div>
            <div class="p mt-10 ultimo">
                Este evento tem como intuito complementar a formação acadêmica dos alunos e discutir temas atuais da
                área da
                Tecnologia da Informação relacionados com o Ensino, Pesquisa e Extensão, além de fatos e episódios
                recentes
                relacionados a aspectos transversais, como Meio Ambiente & Sustentabilidade e Responsabilidade Social. O
                evento
                é gratuito e aberto à comunidade.
            </div>
        </div>
    </div>
</template>

<script setup>
import { onMounted, onUnmounted, ref } from 'vue';
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const larguraTela = ref(window.innerWidth);
let titleTimeline = null;
let pinTrigger = null;

function verificaTela() {
  return larguraTela.value > 800;
}

function initGsapTitle() {
  if (verificaTela() && !titleTimeline) {

    titleTimeline = gsap.timeline({
      scrollTrigger: {
        trigger: "#title",
        toggleActions: "resume pause reverse pause",
        start: "bottom center",
        end: "bottom 50px",
        scrub: 3,
        markers: true,
      },
    });

    titleTimeline.from('#title', {
      x: -100,
      duration: 3,
    });

    pinTrigger = ScrollTrigger.create({
      id: "pinTrigger", // Adicione um ID para facilitar a busca
      trigger: ".title",
      endTrigger: ".description",
      start: "top top",
      end: "bottom 65%",
      pin: true,
      markers: true,
      invalidateOnRefresh: true,
    });

  } else if (!verificaTela()) {
    if (titleTimeline) {
      titleTimeline.kill();
      titleTimeline = null;
    }
    if (pinTrigger) {
      pinTrigger.kill();
      pinTrigger = null;
    }
    gsap.to('#title', { clearProps: "x, position, top, left, bottom, right, width" }); // Limpa as props de pin
  } else if (verificaTela() && titleTimeline && !ScrollTrigger.getById("pinTrigger")) {
    pinTrigger = ScrollTrigger.create({
      id: "pinTrigger",
      trigger: ".title",
      start: "top top",
      end: "bottom 65%",
      pin: true,
      markers: true,
      invalidateOnRefresh: true,
    });
  }
}

onMounted(() => {
  larguraTela.value = window.innerWidth;
  initGsapTitle();

  window.addEventListener('resize', () => {
    
    larguraTela.value = window.innerWidth;
    initGsapTitle();
  });
});

onUnmounted(() => {
  if (titleTimeline) {
    titleTimeline.kill();
    titleTimeline = null;
  }
  if (pinTrigger) {
    pinTrigger.kill();
    pinTrigger = null;
  }
  window.removeEventListener('resize', () => {});
});
</script>


<!-- <script setup>
import { onMounted, ref } from 'vue';
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

const larguraTela = ref(window.innerWidth); // Usar ref para reatividade
let tl = null;
let pintl=null;
onMounted(() => {
    function gsaptitle() {

        if (verificaTela()) {
            tl = gsap.timeline({
                scrollTrigger: {
                    trigger: "#title",
                    toggleActions: "resume pause reverse pause", //quando chega nele / quando passa dele / quando passa e volta nele
                    start: "top center", //elemento e página ou seja começa quando a parte de cima do elemento atinge o centro da pag
                    end: "bottom 50px",
                    scrub: 3, //vai junto com a página / pode ser true ou false ou um valor (suaviza mais)
                },
            });
            pintl = ScrollTrigger.create({
                trigger: ".title",
                endTrigger: ".description",
                start: "top top",
                end: "bottom 65%",
                pin: true,
                markers: true,

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


            tl.from('#title', {
                x: -100,
                duration: 3,
            });
        } else if(!verificaTela() && tl){
            tl.kill();
            tl = null;
            // Reseta os estilos do elemento, se necessário
            gsap.to('#title', { clearProps: "x" });
            if (pintl) {
                pintl.kill();
                pintl = null;
            }
        }
    }
    // gl.to('.description', {
    // y:-230,
    // duration: 1,
    // });



    function verificaTela() {
        return larguraTela.value > 800;
    }


    larguraTela.value = window.innerWidth;

    // Inicializa o GSAP Calendar
    gsaptitle();

    // Adiciona listener para redimensionamento da tela
    window.addEventListener('resize', () => {
        larguraTela.value = window.innerWidth;
        gsaptitle();
    });
})

</script> -->
<style lang="">

</style>