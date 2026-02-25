<script setup>
import { ArrowRight, Sparkles } from 'lucide-vue-next'
</script>

<template>
  <section class="relative overflow-hidden pt-20 pb-24 lg:pt-32 lg:pb-40 bg-[#f8f9fc] dark:bg-slate-950 border-b border-slate-200/80 dark:border-slate-800">
    <!-- Background image container, positioned right, fading left -->
    <div class="absolute right-0 top-0 bottom-0 w-full lg:w-[85%] z-0">
      <img src="../assets/hero-journalism-ai.jpg" alt="" class="w-full h-full object-cover object-center opacity-80 md:opacity-90 dark:opacity-30 pointer-events-none" />
      <!-- Overlay gradient to fade the image into the solid background on the left -->
      <div class="absolute inset-0 bg-gradient-to-r from-[#f8f9fc] via-[#f8f9fc]/80 to-transparent dark:from-slate-950 dark:via-slate-950/80"></div>
      <div class="absolute inset-0 bg-gradient-to-t from-[#f8f9fc] via-transparent to-transparent dark:from-slate-900 border-none"></div>
    </div>

    <!-- Additional background subtle glow to increase contrast for the text if needed -->
    <div class="absolute top-1/2 left-0 -translate-y-1/2 -translate-x-1/4 z-0 rounded-full blur-[140px] opacity-70 bg-white w-[60rem] h-[60rem] pointer-events-none dark:hidden" aria-hidden="true"></div>

    <div class="max-w-[1400px] mx-auto px-4 sm:px-6 lg:px-8 relative z-10 flex">
      <div class="max-w-3xl lg:max-w-4xl xl:max-w-5xl py-10 lg:py-16 xl:py-20">
        <div class="flex items-center text-[15px] font-semibold text-[#4f8bff] mb-5 tracking-wide">
          <Sparkles class="w-5 h-5 mr-2" />
          <span>Manual Profesional por seguridades.org</span>
        </div>
        
        <h1 class="text-5xl md:text-[60px] lg:text-[60px] font-bold tracking-tight text-[#1e293b] dark:text-white mb-6 leading-[1.05]">
          IA para <span class="bg-clip-text text-transparent bg-gradient-to-r from-[#3b82f6] via-[#14b8a6] to-[#059669]">periodistas ninja</span>
        </h1>
        
        <p class="text-[17px] md:text-[19px] lg:text-[21px] text-[#64748b] dark:text-slate-400 mb-9 max-w-[95%] leading-[1.6]">
          Guía completa para integrar inteligencia artificial en tu trabajo periodístico.<br class="hidden lg:block"/>
          Desde avatares y guiones hasta fact-checking, investigación y seguridad<br class="hidden lg:block"/>
          digital.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-3">
          <a href="#avatares" class="bg-[#5a9bff] hover:bg-blue-500 text-white font-medium py-[10px] px-6 rounded-[8px] transition-transform flex items-center justify-center group text-[15px]">
            Comenzar Manual
            <ArrowRight class="ml-2 w-[16px] h-[16px] group-hover:translate-x-1 transition-transform" />
          </a>
          <a href="#seguridad" class="bg-white dark:bg-slate-800 hover:bg-slate-50 dark:hover:bg-slate-700 text-[#1e293b] dark:text-white font-medium py-[10px] px-6 rounded-[8px] transition-transform shadow-[0_2px_8px_-2px_rgba(0,0,0,0.05)] flex items-center justify-center text-[15px]">
            Seguridad Digital
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
