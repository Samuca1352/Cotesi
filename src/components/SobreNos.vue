<template>
    <div class="pages lg:flex md:flex">
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
import { onMounted } from 'vue';
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);


onMounted(() => {
    function gsaptitle() {

        if (verificaTela()) {
            let tl = gsap.timeline({
                scrollTrigger: {
                    trigger: "#title",
                    toggleActions: "resume pause reverse pause", //quando chega nele / quando passa dele / quando passa e volta nele
                    start: "top center", //elemento e página ou seja começa quando a parte de cima do elemento atinge o centro da pag
                    end: "bottom 50px",
                    scrub: 3, //vai junto com a página / pode ser true ou false ou um valor (suaviza mais)
                },
            });
            ScrollTrigger.create({
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
        }
    }
    // gl.to('.description', {
    // y:-230,
    // duration: 1,
    // });



    function verificaTela() {
        const larguraTela = window.innerWidth;

        if (larguraTela > 768) {
            return true;
        }

        return false

    }

    gsaptitle();
})

</script>
<style lang="">

</style>