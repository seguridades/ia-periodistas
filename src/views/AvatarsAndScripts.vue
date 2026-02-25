<script setup>
import { Video } from 'lucide-vue-next'
import ModuleSection from '../components/ui/ModuleSection.vue'
import ToolCard from '../components/ui/ToolCard.vue'
import SecurityAlert from '../components/ui/SecurityAlert.vue'
</script>

<template>
  <ModuleSection 
    id="avatares" 
    chapter="1" 
    title="Avatares y Guiones con IA" 
    subtitle="Aprende a crear presentadores virtuales y generar guiones periodísticos usando herramientas de inteligencia artificial."
    :icon="Video"
  >
    <div class="grid md:grid-cols-2 gap-8 mb-12 text-left">
      <ToolCard title="Herramientas de Anonimato Visual" icon="monitor">
        <ul class="space-y-3 text-slate-600 dark:text-slate-300 text-[15px]">
          <li>
            <a href="https://www.synthesia.io/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Synthesia</a> / 
            <a href="https://www.heygen.com/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">HeyGen</a>: 
            Permiten crear avatares virtuales realistas mediante IA que leen noticias sin exponer tu rostro en cámara. Incluyen voces de alta calidad.
          </li>
          <li>
            <a href="https://lensstudio.snapchat.com/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Filtros AR (Snapchat/Meta)</a>: 
            Opción de bajo costo para distorsionarte en transmisiones, aunque menos seguras frente a software avanzado de ingeniería inversa.
          </li>
          <li>
            <a href="https://www.d-id.com/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">D-ID</a>: 
            Genera presentadores virtuales a partir de ilustraciones artísticas o fotos generadas por IA (ej. Midjourney) para ocular identidades por completo.
          </li>
        </ul>
        <div class="bg-safe-green-bg/50 border border-safe-green/20 rounded-lg p-4 mt-6">
          <h4 class="font-semibold text-safe-green mb-2 text-sm uppercase flex items-center"><span class="w-1.5 h-1.5 rounded-full bg-safe-green mr-2"></span> Mejores Prácticas de Anonimato</h4>
          <ul class="text-sm space-y-2 text-slate-600 dark:text-slate-300 ml-3 list-none">
            <li class="flex items-start"><span class="mr-2 text-safe-green">✓</span> No uses avatares generados a partir de tus propias fotos.</li>
            <li class="flex items-start"><span class="mr-2 text-safe-green">✓</span> Utiliza nombres en clave coherentes para cada avatar virtual.</li>
          </ul>
        </div>
      </ToolCard>

      <ToolCard title="Anonimización de Voz y Guiones" icon="file">
        <ul class="space-y-3 text-slate-600 dark:text-slate-300 text-[15px]">
          <li>
            <a href="https://elevenlabs.io/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">ElevenLabs</a>: 
            Clonación y generación de voz sintética altamente expresiva. Ideal para narrar reportajes sin exponer tu timbre a análisis forense.
          </li>
          <li>
            <a href="https://murf.ai/" target="_blank" rel="noopener noreferrer" class="font-semibold text-brand-blue hover:underline">Murf.ai</a>: 
            Provee un estudio completo con voces pregrabadas de calidad broadcast para documentales, sin necesidad de usar tu voz real como base.
          </li>
          <li>
            <strong class="font-semibold text-slate-800 dark:text-white">Ofuscación de Guiones:</strong> 
            Usa sistemas offline como <a href="https://lmstudio.ai/" target="_blank" rel="noopener noreferrer" class="text-brand-blue hover:underline font-medium">LM Studio</a> o <a href="https://gpt4all.io/" target="_blank" rel="noopener noreferrer" class="text-brand-blue hover:underline font-medium">GPT4All</a> con modelos locales (ej. Llama 3) para revisar y estandarizar tus textos, removiendo modismos sin enviarlos a nubes de terceros.
          </li>
        </ul>
        <div class="bg-brand-blue/5 border border-brand-blue/20 rounded-lg p-4 mt-6">
          <h4 class="font-semibold text-brand-blue mb-2 text-sm uppercase flex items-center"><span class="w-1.5 h-1.5 rounded-full bg-brand-blue mr-2"></span> Consideraciones de Seguridad</h4>
           <ul class="text-sm space-y-2 text-slate-600 dark:text-slate-300 ml-3 list-none">
            <li class="flex items-start"><span class="mr-2 text-brand-blue">✓</span> Usa un VPN al conectarte a estas plataformas (ej. Mullvad).</li>
            <li class="flex items-start"><span class="mr-2 text-brand-blue">✓</span> Paga las suscripciones con tarjetas virtuales o criptomonedas.</li>
          </ul>
        </div>
      </ToolCard>
    </div>

    <SecurityAlert title="Ofuscación de Identidad y Seguridad Operacional (OpSec)" type="critical">
      <div class="grid md:grid-cols-2 gap-6 p-2 text-left">
        <div>
          <h4 class="font-semibold mb-3 border-b-2 inline-block border-alert-red pb-1">Creación de Cuentas:</h4>
          <ul class="space-y-2 text-sm ml-4 list-disc marker:text-alert-red">
            <li>Nunca uses tu correo personal. Usa servicios seguros como <a href="https://proton.me/mail" target="_blank" rel="noopener noreferrer" class="underline font-medium hover:text-red-500">ProtonMail</a> o <a href="https://tuta.com/" target="_blank" rel="noopener noreferrer" class="underline font-medium hover:text-red-500">Tuta</a> y nombres ficticios para registrar los servicios.</li>
            <li>Efectúa los registros de las plataformas desde el navegador anónimo <a href="https://www.torproject.org/" target="_blank" rel="noopener noreferrer" class="font-bold underline hover:text-red-500">Tor Browser</a> o usa un sistema operativo amnésico en USB como <a href="https://tails.net/" target="_blank" rel="noopener noreferrer" class="font-bold underline hover:text-red-500">Tails OS</a>.</li>
            <li>Navega siempre bajo una VPN sin registro de logs auditada independientemente (ej. <a href="https://mullvad.net/" target="_blank" rel="noopener noreferrer" class="underline font-medium hover:text-red-500">Mullvad VPN</a>).</li>
          </ul>
        </div>
        <div>
          <h4 class="font-semibold mb-3 border-b-2 inline-block border-alert-red pb-1">Reporte y Transparencia:</h4>
          <ul class="space-y-2 text-sm ml-4 list-disc marker:text-alert-red">
            <li>Avisa a la audiencia de que usas avatares IA para mantener la confianza pública, pero <strong>jamás reveles</strong> qué herramientas técnicas empleaste.</li>
             <li>Las plataformas comerciales guardan tus prompts y borradores en la nube. Asume siempre que un actor hostil podría solicitar esos datos.</li>
          </ul>
        </div>
      </div>
    </SecurityAlert>
  </ModuleSection>
</template>
