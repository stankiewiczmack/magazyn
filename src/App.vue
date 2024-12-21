<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="min-w-screen min-h-screen overflow-x-hidden antialiased bg-zinc-900 text-white flex flex-col">
    <header class="w-full bg-zinc-800 p-4">
      <nav class="mx-auto container flex gap-4 justify-center">
        <RouterLink to="/">kutas</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </header>

    <main class="w-full flex-1">
      <RouterView />
    </main>
  </div>
</template>
