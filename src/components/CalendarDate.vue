<template>
  <div class="flex flex-wrap items-center justify-center">
    <div>
      <div class="bg-gray-800 text-white p-4 rounded-lg shadow-lg w-80">
        <div class="text-center mb-4 font-bold">MAIO</div>
        <hr class="text-gray-700">
        <div class="grid grid-cols-7">
          <div class="p-2 font-medium text-center text-sm">D</div>
          <div class="text-center p-2 font-medium text-sm">S</div>
          <div class="text-center p-2 font-medium text-sm">T</div>
          <div class="text-center p-2 font-medium text-sm">Q</div>
          <div class="text-center p-2 font-medium text-sm">Q</div>
          <div class="text-center p-2 font-medium text-sm">S</div>
          <div class="text-center p-2 font-medium text-sm">S</div>
          <div></div>
          <div></div>
          <div></div>
          <div></div>
          <button id="day-1" class="p-2 rounded">1</button>
          <button id="day-2" class="p-2 rounded">2</button>
          <button id="day-3" class="p-2 rounded">3</button>
          <button id="day-4" class="p-2 rounded">4</button>
          <button id="day-5" class="p-2 rounded">5</button>
          <button id="day-6" class="p-2 rounded">6</button>
          <button id="day-7" class="p-2 rounded">7</button>
          <button id="day-8" class="p-2">8</button>
          <button id="day-9" class="p-2">9</button>
          <button id="day-10" class="p-2">10</button>
          <button id="day-11" class="p-2">11</button>
          <button id="day-12" @click="selectDay(12)" class="p-2 bg-blue-600 first-date"
            :class="{ selected: selectedDay === 12 && hasBlueBg(12) }">12</button>
          <button id="day-13" @click="selectDay(13)" class="p-2 bg-blue-600"
            :class="{ selected: selectedDay === 13 && hasBlueBg(13) }">13</button>
          <button id="day-14" @click="selectDay(14)" class="p-2 bg-blue-600"
            :class="{ selected: selectedDay === 14 && hasBlueBg(14) }">14</button>
          <button id="day-15" @click="selectDay(15)" class="p-2 bg-blue-600"
            :class="{ selected: selectedDay === 15 && hasBlueBg(15) }">15</button>
          <button id="day-16" @click="selectDay(16)" class="p-2 bg-blue-600 last-date"
            :class="{ selected: selectedDay === 16 && hasBlueBg(16) }">16</button>
          <button id="day-17" class="p-2">17</button>
          <button id="day-18" class="p-2">18</button>
          <button id="day-19" class="p-2">19</button>
          <button id="day-20" class="p-2">20</button>
          <button id="day-21" class="p-2">21</button>
          <button id="day-22" class="p-2">22</button>
          <button id="day-23" class="p-2">23</button>
          <button id="day-24" class="p-2">24</button>
          <button id="day-25" class="p-2">25</button>
          <button id="day-26" class="p-2">26</button>
          <button id="day-27" class="p-2">27</button>
          <button id="day-28" class="p-2">28</button>
          <button id="day-29" class="p-2">29</button>
          <button id="day-30" class="p-2">30</button>
          <button id="day-31" class="p-2">31</button>
        </div>
      </div>
    </div>
    <div class="accordions p-5">

      <!--item 1 //  DIA 12 -->
      <div class="border-b border-slate-200">
        <button v-on:click="toggleAccordion(12)" class="w-full flex justify-between items-center py-5 text-slate-800">
          <span>Dia 1: Abertura / 12 de Maio</span>
          <span id="icon-12" class="text-slate-800 transition-transform duration-300">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="w-4 h-4">
              <path fill-rule="evenodd"
                d="M4.22 6.22a.75.75 0 0 1 1.06 0L8 8.94l2.72-2.72a.75.75 0 1 1 1.06 1.06l-3.25 3.25a.75.75 0 0 1-1.06 0L4.22 7.28a.75.75 0 0 1 0-1.06Z"
                clip-rule="evenodd" />
            </svg>
          </span>
        </button>
        <div id="content-12" class="max-h-0 overflow-hidden transition-all duration-300 ease-in-out">


          <div
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-15 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="https://luvizzotti.com.br/wp-content/uploads/2018/08/luvizzotti-banner-site.png"
              style="position: relative; top:-60px; ">



                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>
          </div>


          <div href="#"
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-25 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="C:\Users\samuelcardoso\Downloads\Design sem nome (1).png" style="position: relative; top:-60px; ">



                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>

          </div>
        </div>


      </div>

      <!--item 2 //  DIA 13 -->
      <div class="border-b border-slate-200">
        <button v-on:click="toggleAccordion(13)" class="w-full flex justify-between items-center py-5 text-slate-800">
          <span>Dia 2 / 13 de Maio

          </span>

          <span id="icon-13" class="text-slate-800 transition-transform duration-300">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="w-4 h-4">
              <path fill-rule="evenodd"
                d="M4.22 6.22a.75.75 0 0 1 1.06 0L8 8.94l2.72-2.72a.75.75 0 1 1 1.06 1.06l-3.25 3.25a.75.75 0 0 1-1.06 0L4.22 7.28a.75.75 0 0 1 0-1.06Z"
                clip-rule="evenodd" />
            </svg>
          </span>
        </button>
        <div id="content-13" class="max-h-0 overflow-hidden transition-all duration-300 ease-in-out">
          <div href="#"
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-15 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="https://luvizzotti.com.br/wp-content/uploads/2018/08/luvizzotti-banner-site.png"
              style="position: relative; top:-60px; ">

                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>

          </div>
          <div href="#"
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-15 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="https://luvizzotti.com.br/wp-content/uploads/2018/08/luvizzotti-banner-site.png"
              style="position: relative; top:-60px; ">

                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>

          </div>
        </div>
      </div>

      <!--item 3 //  DIA 14 -->
      <div class="border-b border-slate-200 ">
        <button v-on:click="toggleAccordion(14)" class="w-full flex justify-between items-center py-5 text-slate-800">
          <span>Dia 3 / 14 de Maio</span>
          <span id="icon-14" class="text-slate-800 transition-transform duration-300">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="w-4 h-4">
              <path fill-rule="evenodd"
                d="M4.22 6.22a.75.75 0 0 1 1.06 0L8 8.94l2.72-2.72a.75.75 0 1 1 1.06 1.06l-3.25 3.25a.75.75 0 0 1-1.06 0L4.22 7.28a.75.75 0 0 1 0-1.06Z"
                clip-rule="evenodd" />
            </svg>

          </span>
        </button>
        <div id="content-14" class="max-h-0 overflow-hidden transition-all duration-300 ease-in-out">
          <div href="#"
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-15 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="https://luvizzotti.com.br/wp-content/uploads/2018/08/luvizzotti-banner-site.png"
              style="position: relative; top:-60px; ">

                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>

          </div>
          <div href="#"
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-15 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="https://luvizzotti.com.br/wp-content/uploads/2018/08/luvizzotti-banner-site.png"
              style="position: relative; top:-60px; ">

                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>

          </div>
        </div>
      </div>

      <!--item 4 //  DIA 15 -->
      <div class="border-b border-slate-200 ">
        <button v-on:click="toggleAccordion(15)" class="w-full flex justify-between items-center py-5 text-slate-800">
          <span>Dia 4 / 15 de Maio</span>
          <span id="icon-15" class="text-slate-800 transition-transform duration-300">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="w-4 h-4">
              <path fill-rule="evenodd"
                d="M4.22 6.22a.75.75 0 0 1 1.06 0L8 8.94l2.72-2.72a.75.75 0 1 1 1.06 1.06l-3.25 3.25a.75.75 0 0 1-1.06 0L4.22 7.28a.75.75 0 0 1 0-1.06Z"
                clip-rule="evenodd" />
            </svg>

          </span>
        </button>
        <div id="content-15" class="max-h-0 overflow-hidden transition-all duration-300 ease-in-out">
          <div href="#"
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-15 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="https://luvizzotti.com.br/wp-content/uploads/2018/08/luvizzotti-banner-site.png"
              style="position: relative; top:-60px; ">

                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>

          </div>
          <div href="#"
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-15 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="https://luvizzotti.com.br/wp-content/uploads/2018/08/luvizzotti-banner-site.png"
              style="position: relative; top:-60px; ">

                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>

          </div>
        </div>
      </div>

      <!--item 5 //  DIA 16 -->
      <div class="border-b border-slate-200 ">

        <button v-on:click="toggleAccordion(16)" class="w-full flex justify-between items-center py-5 text-slate-800">
          <span>Dia 5: Fechamento / 16 de Maio</span>
          <span id="icon-16" class="text-slate-800 transition-transform duration-300">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="w-4 h-4">
              <path fill-rule="evenodd"
                d="M4.22 6.22a.75.75 0 0 1 1.06 0L8 8.94l2.72-2.72a.75.75 0 1 1 1.06 1.06l-3.25 3.25a.75.75 0 0 1-1.06 0L4.22 7.28a.75.75 0 0 1 0-1.06Z"
                clip-rule="evenodd" />
            </svg>

          </span>
        </button>
        <div id="content-16" class="max-h-0 overflow-hidden transition-all duration-300 ease-in-out">
          <div href="#"
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-15 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="https://luvizzotti.com.br/wp-content/uploads/2018/08/luvizzotti-banner-site.png"
              style="position: relative; top:-60px; ">

                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>

          </div>
          <div href="#"
            class="flex sm:flex-wrap lg:flex-nowrap flex-col items-center bg-white border mt-15 border-gray-200 rounded-lg shadow-sm md:flex-row md:max-w-xl hover:bg-gray-100  dark:bg-gray-800 dark:hover:bg-gray-700"
            style="background-color: #0176ff; ">

                <img class=" rounded-t-lg  md:h-60  md:rounded-none md:rounded-s-lg"
              src="https://luvizzotti.com.br/wp-content/uploads/2018/08/luvizzotti-banner-site.png"
              style="position: relative; top:-60px; ">

                <div class="flex relative flex-col cards justify-between p-4 leading-normal">

              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-800 dark:text-white">Noteworthy
                technology acquisitions 2021</h5>

              <p class="mb-3 font-normal text-gray-700 dark:text-gray-900">Here are the biggest enterprise
                technology acquisitions of 2021 so far, in reverse chronological order.</p>
              <button
                class="bg-white hover:bg-blue-500  hover:scale-105 hover:bg-gray-300 transition-all text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded">
                Inscreva-se
              </button>
            </div>

          </div>
        </div>
      </div>

    </div>
  </div>
</template>
<script setup>
import { ref, onMounted } from 'vue';

const selectedDay = ref(null);

onMounted(() => {


  const diaMes = new Date().toLocaleDateString('pt-BR', {
    day: 'numeric'
  })
  selectDay(13); //Descomentar no mês do evento
})
function selectDay(day) {
  selectedDay.value = day;
  toggleAccordion(day)

}

function hasBlueBg(day) {
  const element = document.getElementById(`day-${day}`);
  return element && element.classList.contains('bg-blue-600');
}


function toggleAccordion(index) {
  const content = document.getElementById(`content-${index}`);
  const icon = document.getElementById(`icon-${index}`);

  // SVG for Down icon
  const downSVG = `
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="w-4 h-4">
      <path fill-rule="evenodd" d="M4.22 6.22a.75.75 0 0 1 1.06 0L8 8.94l2.72-2.72a.75.75 0 1 1 1.06 1.06l-3.25 3.25a.75.75 0 0 1-1.06 0L4.22 7.28a.75.75 0 0 1 0-1.06Z" clip-rule="evenodd" />
    </svg>
  `;

  // SVG for Up icon
  const upSVG = `
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" fill="currentColor" class="w-4 h-4">
      <path fill-rule="evenodd" d="M11.78 9.78a.75.75 0 0 1-1.06 0L8 7.06 5.28 9.78a.75.75 0 0 1-1.06-1.06l3.25-3.25a.75.75 0 0 1 1.06 0l3.25 3.25a.75.75 0 0 1 0 1.06Z" clip-rule="evenodd" />
    </svg>
  `;

  // Fechar todos os outros accordions
  for (let i = 12; i <= 16; i++) { // Ajuste os limites conforme necessário
    if (i !== index) {
      const otherContent = document.getElementById(`content-${i}`);
      const otherIcon = document.getElementById(`icon-${i}`);
      if (otherContent && otherContent.style.maxHeight && otherContent.style.maxHeight !== '0px') {
        otherContent.style.maxHeight = '0';
        if (otherIcon) {
          otherIcon.innerHTML = downSVG;
        }
      }
    }
  }

  // Abrir/fechar o accordion selecionado
  if (content.style.maxHeight && content.style.maxHeight !== '0px') {
    content.style.maxHeight = '0';
    icon.innerHTML = downSVG;
  } else {
    content.style.maxHeight = content.scrollHeight + 'px';
    icon.innerHTML = upSVG;
  }


}

</script>

<style scoped>
.first-date {
  border-top-left-radius: 0.5rem;
  border-bottom-left-radius: 0.5rem;
}

.last-date {
  border-top-right-radius: 0.5rem;
  border-bottom-right-radius: 0.5rem;
}

.grid-cols-7 {
  grid-template-columns: repeat(7, 1fr);
}

button.bg-blue-600:hover {
  cursor: pointer;
  /* Adiciona o cursor de ponteiro aos botões */
  background-color: #e2e4e6;
  color: black;
}

button.selected {
  background-color: #e2e4e6;
  color: black;
}
</style>