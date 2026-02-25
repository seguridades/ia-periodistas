<script setup>
import { AlertTriangle, XCircle, CheckCircle } from 'lucide-vue-next'

const props = defineProps({
  title: {
    type: String,
    required: true
  },
  type: {
    type: String,
    default: 'critical', // 'critical', 'warning', 'success'
    validator: (value) => ['critical', 'warning', 'success'].includes(value)
  }
})
</script>

<template>
  <div :class="[
    'border rounded-xl p-6 relative overflow-hidden',
    {
      'bg-alert-red-bg border-alert-red-border text-alert-red': type === 'critical',
      'bg-warn-yellow-bg border-warn-yellow text-warn-yellow': type === 'warning',
      'bg-safe-green-bg border-safe-green text-safe-green': type === 'success'
    }
  ]">
    <div class="flex items-start mb-4">
      <AlertTriangle v-if="type === 'critical' || type === 'warning'" class="w-6 h-6 mr-3 mt-0.5 flex-shrink-0" />
      <CheckCircle v-else class="w-6 h-6 mr-3 mt-0.5 flex-shrink-0" />
      <h3 class="font-bold text-lg" :class="{
        'text-alert-red': type === 'critical',
        'text-amber-600': type === 'warning',
        'text-safe-green': type === 'success'
      }">{{ title }}</h3>
    </div>
    
    <div class="text-slate-800 dark:text-slate-800 text-sm md:text-base space-y-4">
      <slot></slot>
    </div>
  </div>
</template>
