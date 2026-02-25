<script setup>
import { Search, Settings } from 'lucide-vue-next'
import ModuleSection from '../components/ui/ModuleSection.vue'
import ToolCard from '../components/ui/ToolCard.vue'
import WorkflowMap from '../components/ui/WorkflowMap.vue'
import SecurityAlert from '../components/ui/SecurityAlert.vue'

const osintSteps = [
  { title: "Definir Hipótesis", description: "Usa IA para generar hipótesis alternativas basadas en datos preliminares." },
  { title: "Mapear Fuentes", description: "Algoritmos para identificar fuentes potenciales y bases de datos relevantes." },
  { title: "Estrategia de Datos", description: "Planificar qué tipos de análisis de IA aplicar a cada dataset." },
  { title: "Análisis Automático", description: "Procesamiento masivo de datos con algoritmos especializados." },
  { title: "Detección de Patrones", description: "IA para identificar conexiones no evidentes entre datos." },
  { title: "Verificación Cruzada", description: "Validación automática de hallazgos con múltiples fuentes." }
]
</script>

<template>
  <ModuleSection 
    id="investigacion" 
    chapter="3" 
    title="Investigación Periodística con IA" 
    subtitle="Revoluciona tu proceso investigativo usando IA para análisis de datos, búsquedas avanzadas y descubrimiento de conexiones ocultas."
    :icon="Search"
  >
    <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6 mb-12 text-left">
      <ToolCard title="Mapeo Corporativo y Leaks" icon="monitor">
        <ul class="space-y-4 text-[13px] text-slate-600 dark:text-slate-300">
          <li><strong><a href="https://aleph.occrp.org/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">OCCRP Aleph:</a></strong> <p class="text-xs text-slate-500 mt-1">El archivo global definitivo para periodistas. Busca nombres entre millones de registros corporativos, sanciones y bases de datos filtradas.</p></li>
          <li><strong><a href="https://ddosecrets.com/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">DDoSecrets:</a></strong> <p class="text-xs text-slate-500 mt-1">Alternativa a WikiLeaks. Repositorio masivo de correos y documentos oficiales hackeados. (Accede vía Tor).</p></li>
        </ul>
      </ToolCard>

      <ToolCard title="Análisis Masivo de Textos" icon="file">
         <ul class="space-y-4 text-[13px] text-slate-600 dark:text-slate-300">
          <li><strong><a href="https://pinpoint.journaliststudio.google.com/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Google Pinpoint:</a></strong> <p class="text-xs text-slate-500 mt-1">Herramienta gratuita para reporteros que usa IA para extraer nombres, empresas y ubicaciones (NLP) dentro de gigabytes de PDFs o audios filtrados.</p></li>
          <li><strong><a href="https://tesseract-ocr.github.io/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Tesseract OCR local:</a></strong> <p class="text-xs text-slate-500 mt-1">Extrae texto de documentos confidenciales escaneados desde tu terminal, sin subirlos a internet.</p></li>
        </ul>
      </ToolCard>
      
      <ToolCard title="Huella Digital y Scraping" icon="search">
         <ul class="space-y-4 text-[13px] text-slate-600 dark:text-slate-300">
          <li><strong><a href="https://github.com/smicallef/spiderfoot" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Spiderfoot:</a></strong> <p class="text-xs text-slate-500 mt-1">Herramienta de recolección automatizada OSINT. Busca una IP o nombre de usuario en cientos de servidores para armar su perfil.</p></li>
          <li><strong><a href="https://github.com/sherlock-project/sherlock" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Sherlock:</a></strong> <p class="text-xs text-slate-500 mt-1">Script de terminal que rastrea cuentas de redes sociales ocultas bajo un mismo seudónimo a través del mundo.</p></li>
        </ul>
      </ToolCard>
      
      <ToolCard title="Estructuras y Cuadros" icon="monitor">
         <ul class="space-y-4 text-[13px] text-slate-600 dark:text-slate-300">
          <li><strong><a href="https://www.maltego.com/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Maltego:</a></strong> <p class="text-xs text-slate-500 mt-1">El estándar de la industria. Visualiza redes complejas graficando relaciones entre dominios web, empresas fantasma y personas.</p></li>
          <li><strong><a href="https://www.breadcrumbs.app/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Breadcrumbs:</a></strong> <p class="text-xs text-slate-500 mt-1">Rastreador visual open-source para seguir transferencias de Bitcoin o billeteras sospechosas en la blockchain.</p></li>
        </ul>
      </ToolCard>
    </div>

    <div class="grid lg:grid-cols-2 gap-8 items-start text-left mt-8">
      <WorkflowMap id="investigacion-workflow" :steps="[
        { title: 'Crear Sock Puppets', description: 'Crea identidades falsas (Sock Puppets) usando Tor y números VoIP para no investigar desde tu IP y cuenta real.' },
        { title: 'Recolección Pasiva', description: 'Usa motores como Aleph o DDoSecrets para indagar las empresas fantasma u objetivos sin visitar sus servidores directamente.' },
        { title: 'Extracción NLP Activa', description: 'Descarga un leak. Pásalo por Pinpoint o Llama local para encontrar relaciones, nombres cruzados o flujos bancarios.' },
        { title: 'Mapeo Visual (Maltego)', description: 'Une los puntos hallados graficando quién es dueño de qué dominio o billetera criptográfica, formando la evidencia del reportaje.' }
      ]">
        <template #header>
          <div class="mb-6 border-b border-slate-100 dark:border-slate-700 pb-4 text-center">
            <h3 class="text-2xl font-bold mb-2 flex items-center justify-center">
              <span class="bg-brand-blue text-white w-8 h-8 rounded-full flex items-center justify-center text-sm mr-3">WF</span> 
              Metodología OSINT de Exposición Cero
            </h3>
            <p class="text-[15px] text-slate-500 dark:text-slate-400">Pautas seguras para descubrir redes criminales o de corrupción.</p>
          </div>
        </template>
      </WorkflowMap>

      <SecurityAlert title="Ingeniería de Prompts para OSINT" type="warning" class="h-full">
         <div class="space-y-4 flex-grow mt-2">
            <p class="text-[14px] text-slate-700 dark:text-slate-300 leading-relaxed mb-4">
              La forma en que cuestionas a una IA local determina el éxito al auditar megabytes de datos. Emplea estas estructuras:
            </p>
            
            <div class="bg-white/50 dark:bg-slate-800/50 p-4 rounded-lg border border-warn-yellow/20">
              <strong class="text-amber-700 dark:text-amber-500 text-[13px] mb-2 block uppercase tracking-wider">Extracción de Entidades (NER):</strong>
              <code class="block bg-slate-100 dark:bg-slate-900 p-3 rounded text-[12px] text-slate-800 dark:text-slate-200 font-mono leading-relaxed border border-slate-200 dark:border-slate-700">"Actúa como analista de inteligencia. Lee el corpus provisto e identifica entidades. Extrae obligatoriamente: Nombres de Personas, Empresas offshore, Cuentos bancarios y Fechas. Formato: Tabla Markdown."</code>
            </div>

            <div class="bg-white/50 dark:bg-slate-800/50 p-4 rounded-lg border border-warn-yellow/20">
              <strong class="text-amber-700 dark:text-amber-500 text-[13px] mb-2 block uppercase tracking-wider">Lógica Relacional:</strong>
              <code class="block bg-slate-100 dark:bg-slate-900 p-3 rounded text-[12px] text-slate-800 dark:text-slate-200 font-mono leading-relaxed border border-slate-200 dark:border-slate-700">"Analiza este registro de propiedades. Rastrea estructuradamente la cadena corporativa hasta dar con el beneficiario final (UBO). Ignora testaferros listados e identifica al director común entre las Empresas A, B y C."</code>
            </div>
            
            <div class="mt-6 p-4 bg-amber-50 dark:bg-amber-900/10 border-l-4 border-amber-500 rounded-r-lg text-[13px] text-amber-800 dark:text-amber-400 shadow-sm">
              <strong class="font-bold flex items-center mb-1"><Settings class="w-4 h-4 mr-2 text-amber-700 dark:text-amber-500" /> Configuración Crítica:</strong> 
              Al usar modelos en LM Studio u Ollama, establece la <strong>"Temperatura" en 0.0 o 0.1</strong>. Para periodismo de investigación necesitas facticidad algorítmica y cero creatividad o "alucinaciones".
            </div>
         </div>
      </SecurityAlert>
    </div>
  </ModuleSection>
</template>
