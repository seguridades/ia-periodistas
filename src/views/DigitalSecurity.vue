<script setup>
import { ShieldAlert, UserX, Split, MessageSquare, Shield, Laptop, Flame } from 'lucide-vue-next'
import ModuleSection from '../components/ui/ModuleSection.vue'
import ToolCard from '../components/ui/ToolCard.vue'
import SecurityAlert from '../components/ui/SecurityAlert.vue'
</script>

<template>
  <ModuleSection 
    id="seguridad" 
    chapter="4 - Crítico" 
    title="Seguridad Digital Extrema (OPSEC)" 
    subtitle="Protocolos inquebrantables para proteger tu investigación, la identidad de tus fuentes y tus dispositivos físicos al utilizar IA."
    :icon="ShieldAlert"
  >
    <div class="mb-12 text-left">
      <SecurityAlert title="Regla de Oro: Riesgo de Nube" type="critical">
        <p class="font-bold mb-4 text-lg border-b border-alert-red/20 pb-3">NUNCA introduzcas datos crudos sin sanitizar en IAs online:</p>
        <div class="grid md:grid-cols-2 gap-x-12 gap-y-4 max-w-4xl font-medium text-[15px]">
          <ul class="space-y-3">
            <li class="flex items-start"><span class="text-alert-red mr-3 font-bold mt-0.5">✕</span> Nombres reales de informantes en riesgo</li>
            <li class="flex items-start"><span class="text-alert-red mr-3 font-bold mt-0.5">✕</span> Documentos gubernamentales clasificados íntegros</li>
            <li class="flex items-start"><span class="text-alert-red mr-3 font-bold mt-0.5">✕</span> Metadatos GPS de fotografías de reuniones</li>
          </ul>
          <ul class="space-y-3">
            <li class="flex items-start"><span class="text-alert-red mr-3 font-bold mt-0.5">✕</span> Rutas de viaje o ubicaciones seguras</li>
            <li class="flex items-start"><span class="text-alert-red mr-3 font-bold mt-0.5">✕</span> Credenciales de acceso descubiertas en investigaciones</li>
            <li class="flex items-start"><span class="text-alert-red mr-3 font-bold mt-0.5">✕</span> Correos interceptados completos</li>
          </ul>
        </div>
      </SecurityAlert>
    </div>

    <div class="grid md:grid-cols-2 gap-8 mb-12 text-left">
      <div class="bg-white dark:bg-slate-800 rounded-xl overflow-hidden border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col h-full">
        <div class="p-6 border-b border-safe-green/20 bg-safe-green-bg/30">
          <h3 class="text-lg font-bold flex items-center mb-4 text-safe-green">
            <span class="w-2 h-2 rounded-full bg-safe-green mr-3"></span>
            El Arsenal Autónomo (100% Offline)
          </h3>
          <p class="text-[13px] text-slate-600 dark:text-slate-400 mb-4">La única forma segura de analizar leaks masivos con IA es ejecutar modelos localmente sin conexión a internet (Air-Gapped).</p>
          <ul class="space-y-4 text-sm text-slate-700 dark:text-slate-300">
            <li class="flex items-start">
              <span class="text-safe-green mr-2 font-bold mt-0.5">✓</span> 
              <div>
                <a href="https://ollama.com/" target="_blank" rel="noopener noreferrer" class="font-bold hover:underline">Ollama:</a> 
                Ejecuta modelos como Llama 3 o Mistral directamente en tu CPU/GPU. Tus datos nunca salen de tu disco duro.
              </div>
            </li>
            <li class="flex items-start">
              <span class="text-safe-green mr-2 font-bold mt-0.5">✓</span> 
              <div>
                <a href="https://dangerzone.rocks/" target="_blank" rel="noopener noreferrer" class="font-bold hover:underline">Dangerzone:</a> 
                Limpia documentos maliciosos (PDFs filtrados). Los abre en un entorno aislado, quita virus/trackers y te devuelve un PDF seguro.
              </div>
            </li>
            <li class="flex items-start">
              <span class="text-safe-green mr-2 font-bold mt-0.5">✓</span> 
              <div>
                <a href="https://0xacab.org/jvoisin/mat2" target="_blank" rel="noopener noreferrer" class="font-bold hover:underline">MAT2:</a> 
                El kit definitivo para extirpar metadatos invisibles de documentos, imágenes y audios antes de publicarlos.
              </div>
            </li>
          </ul>
        </div>
        <div class="p-6 border-t border-warn-yellow/20 bg-warn-yellow-bg/30 flex-grow">
          <h3 class="text-lg font-bold flex items-center mb-4 text-amber-700 dark:text-amber-500">
            <span class="w-2 h-2 rounded-full bg-amber-500 mr-3"></span>
            Si debes usar la Nube (APIs)
          </h3>
          <p class="text-[13px] text-slate-600 dark:text-slate-400 mb-4">Si tu PC no tiene potencia para IA local y necesitas servicios comerciales para tareas no críticas:</p>
          <ul class="space-y-3 text-sm text-slate-700 dark:text-slate-300">
            <li class="flex items-start">
              <span class="text-amber-500 mr-2 font-bold mt-0.5">!</span> 
              Evita cuentas gratuitas de ChatGPT/Claude, sus Términos de Servicio permiten usar tus textos para entrenar.
            </li>
            <li class="flex items-start">
              <span class="text-amber-500 mr-2 font-bold mt-0.5">!</span> 
              Usa exclusivamente cuentas de desarrollador (APIs de pago) como OpenAI API o Anthropic API. A diferencia de las versiones gratuitas, los contratos de estos servicios de pago prohíben legalmente usar tus textos para entrenar a sus inteligencias artificiales, y te permiten pedir que borren todo rastro en 30 días o menos (Zero Data Retention).
            </li>
          </ul>
        </div>
      </div>

      <ToolCard title="Preparación de Datos Previos a la IA" icon="shield">
         <div class="space-y-5">
           <div>
             <h4 class="font-semibold text-brand-blue flex items-center mb-1"><UserX class="w-4 h-4 mr-2" /> Seudonimización Criptográfica</h4>
             <p class="text-[13px] text-slate-600 dark:text-slate-400 leading-relaxed">Antes de pasar textos a un traductor IA o resumidor, cambia los nombres reales por códigos alfa-numéricos (ej: [Gobernador X] -> [A1]). Desencripta tú mismo el resultado final.</p>
           </div>
           <div>
             <h4 class="font-semibold text-brand-blue flex items-center mb-1"><Split class="w-4 h-4 mr-2" /> Fragmentación de Contexto</h4>
             <p class="text-[13px] text-slate-600 dark:text-slate-400 leading-relaxed">No envíes un plan de investigación completo a una IA. Divide las consultas en fragmentos no correlacionados. Envía dudas financieras en una sesión y dudas legales en otra, usando distintas IPs (circuitos Tor).</p>
           </div>
           <div>
             <h4 class="font-semibold text-brand-blue flex items-center mb-1"><MessageSquare class="w-4 h-4 mr-2" /> Comunicaciones Aisladas</h4>
             <p class="text-[13px] text-slate-600 dark:text-slate-400 leading-relaxed">Pacta y entrevista a tus fuentes usando <a href="https://signal.org/" target="_blank" rel="noopener noreferrer" class="underline font-semibold hover:text-brand-blue">Signal</a> (con mensajes efímeros) o <a href="https://simplex.chat/" target="_blank" rel="noopener noreferrer" class="underline font-semibold hover:text-brand-blue">Session / SimpleX</a>. No dictes el audio confidencial cerca de tu teléfono con asistentes de voz activos.</p>
           </div>
         </div>
      </ToolCard>
    </div>

    <!-- Security Protocol Timeline -->
    <div class="bg-white dark:bg-slate-800 rounded-xl p-8 border border-slate-200 dark:border-slate-700 mb-12 shadow-sm text-center">
      <h3 class="text-2xl font-bold mb-10">Ciclo Operativo de Defensa (OPSEC)</h3>
      <div class="grid md:grid-cols-3 gap-8 relative items-stretch">
        <div class="hidden md:block absolute top-[28px] left-[10%] right-[10%] h-[3px] bg-slate-100 dark:bg-slate-700 z-0"></div>
        
        <!-- Step 1 -->
        <div class="relative z-10 flex flex-col h-full">
          <div class="w-14 h-14 mx-auto bg-slate-50 dark:bg-slate-800 rounded-full flex items-center justify-center border-4 border-white dark:border-slate-900 mb-4 shadow-sm relative shrink-0">
            <Shield class="w-6 h-6 text-slate-700 dark:text-slate-300" />
          </div>
          <h4 class="font-bold text-lg mb-4 text-slate-900 dark:text-white shrink-0">1. Aislamiento</h4>
          <div class="bg-brand-blue/5 border border-brand-blue/20 rounded-lg p-5 text-left text-[14px] space-y-3 flex-grow">
             <div>
               <strong class="block text-brand-blue mb-1">Máquinas Virtuales</strong>
               <span class="text-slate-600 dark:text-slate-400">Si debes correr riesgos, aísla el entorno de IA en una VM amnésica como <a href="https://www.whonix.org/" target="_blank" rel="noopener noreferrer" class="font-semibold hover:underline">Whonix</a>, que enruta todo su tráfico obligatoriamente a través de Tor.</span>
             </div>
          </div>
        </div>

        <!-- Step 2 -->
        <div class="relative z-10 flex flex-col h-full">
          <div class="w-14 h-14 mx-auto bg-slate-50 dark:bg-slate-800 rounded-full flex items-center justify-center border-4 border-white dark:border-slate-900 mb-4 shadow-sm relative shrink-0">
            <Laptop class="w-6 h-6 text-slate-700 dark:text-slate-300" />
          </div>
          <h4 class="font-bold text-lg mb-4 text-slate-900 dark:text-white shrink-0">2. Ejecución Local</h4>
          <div class="bg-safe-green-bg/30 border border-safe-green/20 rounded-lg p-5 text-left text-[14px] space-y-3 flex-grow">
             <div>
               <strong class="block text-safe-green mb-1">Air-Gapping</strong>
               <span class="text-slate-600 dark:text-slate-400">Para clasificados, desconecta físicamente el Wi-Fi/cable del portátil. Procesa los PDFs usando un LLM instalado previamente. Mueve los resultados en USBs encriptados.</span>
             </div>
          </div>
        </div>

        <!-- Step 3 -->
        <div class="relative z-10 flex flex-col h-full">
          <div class="w-14 h-14 mx-auto bg-slate-50 dark:bg-slate-800 rounded-full flex items-center justify-center border-4 border-white dark:border-slate-900 mb-4 shadow-sm relative shrink-0">
            <Flame class="w-6 h-6 text-slate-700 dark:text-slate-300" />
          </div>
          <h4 class="font-bold text-lg mb-4 text-slate-900 dark:text-white shrink-0">3. Destrucción</h4>
          <div class="bg-alert-red-bg/30 border border-alert-red/20 rounded-lg p-5 text-left text-[14px] space-y-3 flex-grow">
             <div>
               <strong class="block text-alert-red mb-1">Cifrado y Borrado Crítico</strong>
               <span class="text-slate-600 dark:text-slate-400">Jamás uses "Eliminar" normal. Usa <a href="https://www.bleachbit.org/" target="_blank" rel="noopener noreferrer" class="font-semibold hover:underline text-alert-red">BleachBit</a> para sobrescribir los datos temporal de la IA. Guarda tu nota final en un volumen oculto de <a href="https://www.veracrypt.fr/" target="_blank" rel="noopener noreferrer" class="font-semibold hover:underline text-alert-red">VeraCrypt</a>.</span>
             </div>
          </div>
        </div>
      </div>
    </div>
  </ModuleSection>
</template>
