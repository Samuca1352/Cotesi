<template>
    <div class="bg-white border-gray-200 dark:bg-neutral-800 flex justify-center dark:text-white pt-10">
        <div class="container ">
            <HeaderPage></HeaderPage>
        </div>
    </div>
    <div class="">
    <div class="red h-screen panel flex items-center justify-center" style=" background-color: red;">
                Espaço para simular conteúdo longo
            </div>
    <div class="blue h-screen panel  flex items-center justify-center" style=" background-color: blue;">
                Mais espaço para simular conteúdo longo
            </div>
    <div class="pink h-screen panel  flex items-center justify-center" style=" background-color: pink;">
                Mais espaço para simular conteúdo longo
            </div>
    <div class="black h-screen panel  flex items-center justify-center" style=" background-color: black;">
                Mais espaço para simular conteúdo longo
            </div>
        </div>
</template>
<script setup>
import HeaderPage from './components/HeaderPage.vue';
import { gsap } from "gsap";
import { onMounted } from 'vue';
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);




onMounted(() => {
    /*let tl = gsap.timeline({
    scrollTrigger: {
        trigger: ".c",
        toggleActions: "restart pause reverse pause", //quando chega nele / quando passa dele / quando passa e volta nele
        start: "top center", //elemento e página ou seja começa quando a parte de cima do elemento atinge o centro da pag
        end: "bottom 100px",
        scrub: 3, //vai junto com a página / pode ser true ou false ou um valor (suaviza mais)
        markers: true, //marcadores
        pin: true, // fixa o elemento na tela enquanto realiza
    },
});
    tl.to('.c', {

        x: 400,
        duration: 3,
    });*/

    /*ScrollTrigger.create({
        trigger: ".red",
        start:"top top",
        end: "+=300px",
        pinSpacing:false,
        pin:true,
    })*/

    gsap.utils.toArray(".panel").forEach((panel, i)=>{
        ScrollTrigger.create({
        trigger: panel,
        start:"top top",
        pinSpacing:false,
        pin:true,
    })
    })


})
</script>

<style>
body{
    overflow-x: hidden ;
}
</style>
