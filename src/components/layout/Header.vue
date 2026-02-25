<script setup>
import { BookOpen, ShieldAlert } from 'lucide-vue-next'
</script>

<template>
  <header class="sticky top-0 z-50 w-full h-[65px] flex flex-col justify-center backdrop-blur-xl flex-none transition-colors duration-500 lg:z-50 bg-[#f8f9fc]/60 supports-backdrop-blur:bg-white/40 dark:bg-slate-900/60 border-b border-[#e2e8f0]/40 dark:border-slate-800 shadow-sm">
    <div class="max-w-[1400px] w-full mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between">
        <a class="flex items-center space-x-3 text-slate-800 dark:text-white" href="/">
          <!-- Recreating the exact blue icon from the image -->
          <div class="w-9 h-9 flex items-center justify-center text-blue-500 rounded hover:scale-105 transition-transform">
            <svg class="w-7 h-7" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
              <path d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"></path>
              <path d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"></path>
            </svg>
          </div>
          <div class="leading-tight flex flex-col justify-center">
            <span class="block text-xl font-extrabold tracking-tight">
              <span class="text-slate-700 dark:text-slate-200">IA para </span>
              <span class="bg-clip-text text-transparent bg-gradient-to-r from-[#3b82f6] via-[#14b8a6] to-[#059669]">periodistas ninja</span>
            </span>
            <span class="block text-[13px] text-slate-400 font-medium tracking-wide">seguridades.org</span>
          </div>
        </a>
        <div class="flex items-center space-x-6">
          <nav class="hidden md:flex space-x-8 text-[14px] font-medium text-slate-500 dark:text-slate-400">
            <a href="#avatares" class="hover:text-blue-500 dark:hover:text-white transition-colors">Avatares & Guiones</a>
            <a href="#fact-checking" class="hover:text-blue-500 dark:hover:text-white transition-colors">Fact Checking</a>
            <a href="#investigacion" class="hover:text-blue-500 dark:hover:text-white transition-colors">Investigación</a>
            <a href="#seguridad" class="hover:text-blue-500 dark:hover:text-white transition-colors">Seguridad Digital</a>
          </nav>
        </div>
      </div>
    </div>
  </header>
</template>
