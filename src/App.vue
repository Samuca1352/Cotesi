<template>
    <div class="container">
      <div class="text-container">
        <h1 class="zooming-text">TEXTO EM CAIXA ALTA</h1>
      </div>
      <div class="content">
        <p>Este é o conteúdo que rola após o efeito.</p>
      </div>
    </div>
  </template>
<script setup>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { onMounted } from 'vue';

gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
  let zoomingText = document.querySelector('.zooming-text');
  let container = document.querySelector('.container');

  gsap.to(zoomingText, {
    scale: 10, // Aumenta o tamanho do texto
    scrollTrigger: {
      trigger: '.text-container',
      start: 'top top',
      end: 'bottom top',
      scrub: true, // Animação suave durante o scroll
      pin: true, // Fixa o texto na tela
      onUpdate: (self) => {
        if (self.progress > 0.8) { // Altera a cor de fundo quando o zoom estiver quase completo
          container.style.backgroundColor = '#000000'; // Muda para preto
        } else {
          container.style.backgroundColor = '#ffffff'; // Mantém branco antes do zoom completo
        }
      },
    },
  });
});
</script>


<style>
html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  overflow-x: hidden;
}

.container {
  width: 100%;
  min-height: 300vh; /* Altura mínima para simular scroll */
  font-family: sans-serif;
  background-color: #ffffff; /* Cor de fundo inicial branca */
  transition: background-color 0.5s ease; /* Transição suave para a cor de fundo */
}

.text-container {
  position: sticky;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10; /* Garante que o texto fique na frente */
}

.zooming-text {
  font-size: 2em;
  text-transform: uppercase;
  color: #000000; /* Cor do texto inicial preta */
}

.content {
  padding: 20px;
}
</style>
