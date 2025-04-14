<template>
  <div  class="h-full w-full mb-15 pt-15">

    <h3 class="relative text-center mb-4 font-black  text-gray-800 sm:text-5xl xl:mb-8 mb-5">APOIADORES</h3>

    <swiper   :slides-per-view="3" :breakpoints="{768: {slidesPerView: 5,  },  
    }" 
    :centered-slides="true"
    :loop="true"
    :autoplay="{ // Configurações do autoplay
        delay: 2000, // Tempo em milissegundos entre os slides (opcional, padrão é 3000)
        disableOnInteraction: false, // Permite que o autoplay continue mesmo após a interação do usuário (opcional, padrão é true)
        pauseOnMouseEnter: true, // Pausa o autoplay ao passar o mouse (opcional, padrão é false)
        // reverseDirection: false, // Descomente para inverter a direção (opcional, padrão é false)
      }"
    :navigation="navigationEnabled ? { hideOnClick: true } : larguraTela>768"
    :pagination="{
      hideOnClick: true
    }"
      class="h-full overflow-x-hidden w-full select-none ">

      
      <swiper-slide>
        <div class="ts-swiper "><img loading="lazy" src="../img/patrocinadores/facchini-logo.png" alt="Logo Facchini"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img loading="lazy"  src="../img/patrocinadores/flash-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper "><img loading="lazy" src="../img/patrocinadores/facchini-logo.png" alt="Logo Facchini"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img loading="lazy"  src="../img/patrocinadores/flash-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper "><img loading="lazy" src="../img/patrocinadores/facchini-logo.png" alt="Logo Facchini"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img loading="lazy"  src="../img/patrocinadores/flash-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper "><img loading="lazy" src="../img/patrocinadores/facchini-logo.png" alt="Logo Facchini"></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img loading="lazy"  src="../img/patrocinadores/flash-logo.png" alt=""></div>
      </swiper-slide>
      

    </swiper>

    
  </div>
</template>
<script setup>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// import Swiper core and required modules
// swiper bundle styles
import "swiper/element/css/autoplay"
import "swiper/css/bundle";
import { onMounted,ref } from 'vue';

const autoplayConfig = ref(false); // Inicialmente desabilitado

const larguraTela = ref(window.innerWidth); // Usar ref para reatividade



</script>
<style scoped>
.ts-swiper {
  max-width: 200px; /* Ajuste este valor conforme necessário */
  margin-left: auto;
  margin-right: auto; /* Para centralizar o conteúdo dentro do slide */
}



.swiper-slide {
  /* Estilos base dos seus slides */
  opacity: 0.95; /* Opcional: para dar um destaque menor aos outros slides */
  transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out; /* Adiciona uma transição suave */
}

.swiper-slide-active {
  transform: scale(1.3); /* Aumenta o tamanho do slide ativo em 10% */
  opacity: 1; /* Garante que o slide ativo esteja totalmente visível */
  z-index: 1; /* Garante que o slide ativo não seja sobreposto pelos vizinhos */
  transform: translateY(-2px);
}
</style>