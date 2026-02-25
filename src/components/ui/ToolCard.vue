<script setup>
import { Monitor, FileText, Search, Shield } from 'lucide-vue-next'

const props = defineProps({
  title: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    default: 'monitor' // 'monitor', 'file', 'search', 'shield'
  }
})
</script>

<template>
  <div class="bg-white dark:bg-slate-800 border border-slate-100 dark:border-slate-800 rounded-2xl p-8 shadow-xl shadow-slate-200/40 dark:shadow-none hover:-translate-y-1 hover:shadow-2xl hover:shadow-slate-200/60 transition-all duration-300">
    <div class="flex items-center mb-6">
      <div class="w-10 h-10 rounded-lg bg-brand-blue/10 flex items-center justify-center mr-4 text-brand-blue">
        <Monitor v-if="icon === 'monitor'" class="w-5 h-5" />
        <FileText v-else-if="icon === 'file'" class="w-5 h-5" />
        <Search v-else-if="icon === 'search'" class="w-5 h-5" />
        <Shield v-else class="w-5 h-5" />
      </div>
      <h3 class="text-xl font-bold text-slate-900 dark:text-white">{{ title }}</h3>
    </div>
    <div class="space-y-4">
      <slot></slot>
    </div>
  </div>
</template>
