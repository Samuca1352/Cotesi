<template>
  <div class="h-full">
    <swiper :slides-per-view="3" :breakpoints="{768: {slidesPerView: 5, },
    }" 
    :centered-slides="true"
    :loop="true"
    :Autoplay="true"
    :navigation="{ hideOnClick:true}"
    :pagination="{
      hideOnClick: true
    }"
      class="h-full select-none">
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
      <swiper-slide>
        <div class="ts-swiper"><img src="../img/facchini-logo.png" alt=""></div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script setup>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// import Swiper core and required modules
// swiper bundle styles
import "swiper/css/bundle";
import { onMounted } from 'vue';
import { Autoplay } from "swiper/modules";




onMounted(() => {


})


</script>
<style scoped>
.ts-swiper {
  text-align: center;
  padding: 5vh;
}




.swiper-slide {
  /* Estilos base dos seus slides */
  opacity: 0.95; /* Opcional: para dar um destaque menor aos outros slides */
  transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out; /* Adiciona uma transição suave */
}

.swiper-slide-active {
  transform: scale(1.5); /* Aumenta o tamanho do slide ativo em 10% */
  opacity: 1; /* Garante que o slide ativo esteja totalmente visível */
  z-index: 1; /* Garante que o slide ativo não seja sobreposto pelos vizinhos */
}
</style>