<script setup>
import { ref, watch, onMounted } from 'vue'
import { Check } from 'lucide-vue-next'

const props = defineProps({
  id: {
    type: String,
    required: true
  },
  steps: {
    type: Array,
    required: true
  }
})

const completedSteps = ref([])

onMounted(() => {
  const saved = localStorage.getItem(`workflow-${props.id}`)
  if (saved) {
    completedSteps.value = JSON.parse(saved)
  }
})

watch(completedSteps, (newVal) => {
  localStorage.setItem(`workflow-${props.id}`, JSON.stringify(newVal))
}, { deep: true })

const toggleStep = (index) => {
  const pos = completedSteps.value.indexOf(index)
  if (pos !== -1) {
    completedSteps.value.splice(pos, 1)
  } else {
    completedSteps.value.push(index)
  }
}
</script>

<template>
  <div class="bg-white dark:bg-slate-800 rounded-2xl shadow-xl shadow-slate-200/40 dark:shadow-none border border-slate-100 dark:border-slate-800 p-8 md:p-10">
    <slot name="header"></slot>
    <div class="relative mt-8">
      <div class="absolute left-[23px] top-4 bottom-4 w-0.5 bg-slate-200 dark:bg-slate-700" aria-hidden="true"></div>
      <ul class="space-y-8 relative">
        <li v-for="(step, index) in steps" :key="index" class="relative pl-14">
          <button @click="toggleStep(index)" class="absolute left-0 top-0 w-12 h-12 rounded-full border-2 flex items-center justify-center transition-colors bg-white dark:bg-slate-800" 
            :class="completedSteps.includes(index) ? 'border-brand-blue text-brand-blue bg-brand-blue/10' : 'border-slate-300 dark:border-slate-600 text-slate-400 hover:border-brand-blue/50 hover:text-brand-blue'">
            <Check v-if="completedSteps.includes(index)" class="w-6 h-6" />
            <span v-else class="text-lg font-medium">{{ index + 1 }}</span>
          </button>
          
          <div class="pt-2 transition-opacity" :class="completedSteps.includes(index) ? 'opacity-50' : ''">
            <h4 class="text-xl font-bold text-slate-900 dark:text-white mb-2" :class="{'line-through': completedSteps.includes(index)}">{{ step.title }}</h4>
            <p class="text-slate-600 dark:text-slate-400 text-sm">{{ step.description }}</p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
