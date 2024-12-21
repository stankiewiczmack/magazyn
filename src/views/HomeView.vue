<script setup>
import { ref } from 'vue'

const dane = [
  [
    'cos',
    'ktos',
    'dupa 1',
    'dupa 2',
  ],
  [
    'cos',
    'ktos',
    'dupa 1',
    'dupa 2',
  ],
  [
    'cos',
    'ktos',
    'dupa 1',
    'dupa 2',
  ],
];

// przydatne linki
// https://vuejs.org/guide/essentials/lifecycle
// do zapytań użyjesz axios, musisz go doinstalować (wiesz jak paczke 'npm install nazwapaczki', musisz znaleźć do tego tutorial na necie)
// poczytaj co to w vue jest:
// ref, v-for / :key, v-if, v-show, onMounted, jak pisać funkcje, co to const, let, co to tablica i obiekt, co to zmienne
// co to jest tailwind? https://www.youtube.com/watch?v=mr15Xzb1Ook
// co to jest vue? https://www.youtube.com/watch?v=nhBVL41-_Cw

// tutaj dokumentacja tailwinda: https://tailwindcss.com/docs/installation
// tutaj jest dokumentacja vue: https://vuejs.org/guide/introduction.html

// tu jest tutorial do vue na youtube: https://www.youtube.com/watch?v=YrxBCBibVo0&list=PL4cUxeGkcC9hYYGbV60Vq3IXYNfDk8At1
// tu jest tutorial do tailwindcss: https://www.youtube.com/watch?v=bxmDnn7lrnk&list=PL4cUxeGkcC9gpXORlEHjc5bgnIi5HEGhw


// nie dajesz se rady z open weather api? tu jest tutorial krok po kroku: https://www.youtube.com/watch?v=MdIfZJ08g2I
// nie wiesz za chuja co to axios i jak robić zapytania do open weather api? tu jest tutorial: https://www.youtube.com/watch?v=k8hrLNnhZS4

// co mam zrobić
// w tym miejscu masz po api zaciągnąć dane pogodowe ze strony https://openweathermap.org/, robisz tam konto, 
// z niego masz token do url, tutaj używasz tego url do zaciągania danych, podstawiasz je pod zmienną
// i następnie wyświetlasz te dane "jeżeli są" w widoku
// nastepnie
// widok ma zawierać pole input do wpisywania tekstu
// jak wpiszesz tekst i wciśniesz guzik "pokaż prognozę", wywoła to zapytanie które zrobiłeś wcześniej
// ale z parametrem którym jest 'miasto'
// jak dane zwróci i będą no to je wyświetla
// bazowo po wejściu na strone ma się wyświetlić pogoda z losowego miasta bądź aktualnego w którym jesteś
// następnie
// jeżeli pada bądź słonecznie bądź chuj wie ma się pojawić adekwatna do tego statusu ikona np słoneczko albo chmurka itd itp
// format widoku to:

// Pole Tekstowe
// Guzik
// Ikona
// Temperatura w Celciuszach
// Nazwa miejscowości

const danePogodowe = ref({});

const pobierzDanePogodowe = () => {
  // Tu pobierzesz dane pogodowe i podstawisz do zmiennej

  danePogodowe.value = {};
};


</script>

<template>
  <main class="container mx-auto mt-10">
    
    <div class="mx-auto">
      <p class="text-center">To jest strona główna</p>
      <p class="text-center">tu będzie wyświetlana pogoda</p>
    </div>

    <h1 class="text-3xl text-center pt-10">Jak dodać i używać dane dane?</h1>
    <p v-for="text in dane" :key="text">{{text[2]}}</p>
    <p class="text-3xl text-red-500">kolor jakis</p>

    <input
      type="text"
      class="p-1 rounded-full bg-zinc-700"
    >
    <button class="bg-blue-500">Pobierz Dane Pogodowe</button>
    <p>{{danePogodowe}}</p>
  </main>
</template>
