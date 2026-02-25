<script setup>
import { ShieldCheck } from 'lucide-vue-next'
import ModuleSection from '../components/ui/ModuleSection.vue'
import ToolCard from '../components/ui/ToolCard.vue'
import WorkflowMap from '../components/ui/WorkflowMap.vue'
import SecurityAlert from '../components/ui/SecurityAlert.vue'

const verificationSteps = [
  { title: "Identificación de Claims", description: "Usa IA para detectar afirmaciones verificables automáticamente." },
  { title: "Búsqueda de Evidencias", description: "Herramientas de IA buscan fuentes y evidencias relacionadas." },
  { title: "Análisis y Verificación", description: "Comparación automática con bases de datos confiables." },
  { title: "Revisión Humana", description: "Validación final por periodistas especializados." }
]
</script>

<template>
  <ModuleSection 
    id="fact-checking" 
    chapter="2" 
    title="Fact Checking con IA" 
    subtitle="Utiliza herramientas de IA para verificar información, detectar desinformación y acelerar el proceso de fact-checking periodístico."
    :icon="ShieldCheck"
  >
    <div class="grid md:grid-cols-3 gap-6 mb-12 text-left">
      <ToolCard title="Verificación Reversa e Imagen" icon="search">
        <ul class="space-y-3 text-sm text-slate-600 dark:text-slate-300 list-disc ml-4">
          <li><a href="https://www.invid-project.eu/tools-and-services/invid-verification-plugin/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">InVID / WeVerify:</a> Extensión clave para fragmentar video y detectar manipulaciones.</li>
          <li><a href="https://tineye.com/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">TinEye</a> / <a href="https://lens.google.com/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Google Lens:</a> Búsqueda reversa indispensable para desmentir fotos recicladas.</li>
          <li><a href="https://toolbox.google.com/factcheck/explorer" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Fact Check Explorer:</a> Buscador de desmentidos globales ya trabajados por agencias.</li>
        </ul>
      </ToolCard>
      
      <ToolCard title="Análisis Forense Offline" icon="file">
         <ul class="space-y-3 text-sm text-slate-600 dark:text-slate-300 list-disc ml-4">
          <li><a href="https://exiftool.org/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">ExifTool:</a> La herramienta definitiva y local (sin internet) para extraer o borrar metadatos ocultos (GPS, cámara, autor) de cualquier archivo.</li>
          <li><a href="https://29a.ch/photo-forensics/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Forensically:</a> Lupa de clonación y análisis de niveles de error (ELA) para detectar si una imagen fue alterada con Photoshop o IA.</li>
        </ul>
      </ToolCard>

      <ToolCard title="Preservación de Evidencia" icon="monitor">
         <ul class="space-y-3 text-sm text-slate-600 dark:text-slate-300 list-disc ml-4">
          <li>
            <strong class="font-semibold text-slate-800 dark:text-white">Archivadores Web:</strong> Usa 
            <a href="https://archive.today/" target="_blank" rel="noopener noreferrer" class="text-brand-blue hover:underline">Archive.today</a> para capturar artículos locales con paywalls pesados o redes sociales volátiles, y recurre a 
            <a href="https://archive.org/web/" target="_blank" rel="noopener noreferrer" class="text-brand-blue hover:underline">Wayback Machine</a> para preservar portales gubernamentales enteros o demostrar estructuras históricas de webs institucionales. Usa ambas para redundancia.
          </li>
          <li><a href="https://hashes.com/en/tools/hash_generator" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Generadores Hash:</a> Crea firmas criptográficas (SHA-256) de tus videos/fotos filtrados para probar que no los alteraste después de recibirlos.</li>
        </ul>
      </ToolCard>
    </div>

    <div class="grid lg:grid-cols-2 gap-8 items-start text-left">
      <WorkflowMap id="fact-checking-workflow" :steps="[
        { title: 'Custodia Cero', description: 'Descarga el archivo sospechoso a un pendrive/disco encriptado. No lo abras directo en tu PC principal.' },
        { title: 'Extracción Offline', description: 'Abre ExifTool sin internet. Extrae los metadatos y revisa huellas del autor o geolocalización.' },
        { title: 'Búsqueda Inversa Segura', description: 'Usa una VPN. Sube el video a InVID o la foto a TinEye comprobando si ya existía antes.' },
        { title: 'Archivado Inmutable', description: 'Si la fuente o el autor borra el post original, asegúrate de haber creado una copia en Archive.today.' }
      ]">
        <template #header>
          <div class="mb-6 border-b border-slate-100 dark:border-slate-700 pb-4">
            <h3 class="text-2xl font-bold mb-2 flex items-center">
              <span class="bg-brand-blue text-white w-8 h-8 rounded-full flex items-center justify-center text-sm mr-3">WF</span> 
              Flujo Seguro de Verificación
            </h3>
            <p class="text-[15px] text-slate-500 dark:text-slate-400">Guía paso a paso para procesar material filtrado minimizando el riesgo (estado local guardado).</p>
          </div>
        </template>
      </WorkflowMap>

      <SecurityAlert title="Precaución al subir Documentos Filtrados" type="critical" class="h-full">
        <ul class="space-y-6 flex-grow">
          <li class="bg-white/50 dark:bg-slate-800/50 p-4 rounded-lg border border-alert-red/20">
            <strong class="text-alert-red dark:text-red-400 flex items-center"><span class="w-1.5 h-1.5 rounded-full bg-alert-red mr-2"></span> El peligro de ChatGPT o VirusTotal</strong>
            <p class="text-sm mt-3 text-slate-700 dark:text-slate-300 leading-relaxed">
              <strong>NUNCA</strong> subas documentos PDF clasificados, audios filtrados o bases de datos a herramientas online (como ChatGPT, Claude, o escáneres online) para que te los "resuman" o verifiquen. Las agencias de inteligencia monitorean estos puentes y los términos de servicio de estas IAs les permiten quedarse con tus exclusivas o exponer a tu informante.
            </p>
          </li>
          <li class="bg-white/50 dark:bg-slate-800/50 p-4 rounded-lg border border-warn-yellow/20">
            <strong class="text-amber-700 dark:text-amber-500 flex items-center"><span class="w-1.5 h-1.5 rounded-full bg-amber-500 mr-2"></span> Análisis Aislado</strong>
            <p class="text-sm mt-2 text-slate-700 dark:text-slate-300 leading-relaxed">Si necesitas IA para analizar miles de páginas de un leak, usa un portátil secundario sin conexión a internet (air-gapped) ejecutando modelos locales pequeños.</p>
          </li>
        </ul>
      </SecurityAlert>
    </div>
  </ModuleSection>
</template>
