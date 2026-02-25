<script setup>
import { RouterView } from 'vue-router'
import Header from './components/layout/Header.vue'
import Footer from './components/layout/Footer.vue'
</script>

<template>
  <div class="min-h-screen flex flex-col font-sans text-slate-800 dark:text-slate-200">
    <Header />
    <main class="flex-grow">
      <RouterView />
    </main>
    <Footer />
  </div>
</template>
