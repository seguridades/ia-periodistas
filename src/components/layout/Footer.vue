<script setup>
import { BookOpen, Github } from 'lucide-vue-next'
</script>

<template>
  <footer class="bg-slate-900 border-t border-slate-800 text-slate-400 py-12">
    <div class="max-w-[1400px] mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div class="col-span-1 lg:col-span-2">
          <a class="flex items-center space-x-2 font-bold text-white mb-4" href="/">
            <BookOpen class="w-6 h-6 text-brand-blue" />
            <span class="text-xl">IA para periodistas ninja</span>
          </a>
          <p class="text-sm mb-4">Una iniciativa de seguridades.org</p>
          <p class="text-sm max-w-sm mb-6">
            Manual profesional para integrar inteligencia artificial en el periodismo de manera ética, segura y efectiva. Disponible bajo licencia Creative Commons.
          </p>
          <div class="flex flex-wrap gap-3 mt-4">
            <a href="https://seguridades.org" target="_blank" rel="noopener noreferrer" class="text-slate-400 hover:text-white border border-slate-700/80 hover:border-slate-500 rounded px-3 py-1.5 text-xs transition-colors">seguridades.org</a>
            <a href="https://github.com/seguridades/ia-periodistas" target="_blank" rel="noopener noreferrer" class="text-slate-400 hover:text-white border border-slate-700/80 hover:border-slate-500 rounded px-3 py-1.5 text-xs flex items-center gap-1.5 transition-colors">
              <Github class="w-3.5 h-3.5" />
              Ver Código Fuente
            </a>
            <span class="text-slate-500 border border-transparent px-1 py-1.5 text-xs">CC BY-SA 4.0</span>
          </div>
        </div>
        
        <div>
          <h3 class="text-white font-semibold mb-4">Capítulos</h3>
          <ul class="space-y-3 text-sm">
            <li><a href="#avatares" class="hover:text-brand-blue">Avatares y Guiones</a></li>
            <li><a href="#fact-checking" class="hover:text-brand-blue">Fact Checking con IA</a></li>
            <li><a href="#investigacion" class="hover:text-brand-blue">Investigación Periodística</a></li>
            <li><a href="#seguridad" class="hover:text-alert-red flex items-center">Seguridad Digital</a></li>
          </ul>
        </div>

        <div>
           <h3 class="text-white font-semibold mb-4">Recursos</h3>
           <ul class="space-y-3 text-sm">
             <li><a href="#" class="hover:text-white">Guías de Herramientas</a></li>
             <li><a href="#" class="hover:text-white">Mejores Prácticas</a></li>
             <li><a href="#" class="hover:text-white">Casos de Estudio</a></li>
           </ul>
        </div>
      </div>
      
      <div class="mt-12 pt-8 border-t border-slate-800 flex flex-col md:flex-row justify-between items-center text-xs">
        <p>© 2026 seguridades.org - Manual bajo licencia Creative Commons BY-SA 4.0. Libre para compartir y adaptar con atribución.</p>
        <div class="flex items-center space-x-4 mt-4 md:mt-0">
           <a href="#" class="hover:text-white">Conocimiento Libre</a>
        </div>
      </div>
    </div>
  </footer>
</template>
