<script setup>
const props = defineProps({
  id: String,
  chapter: String,
  title: String,
  subtitle: String,
  icon: [Object, Function]
})
</script>

<template>
  <section :id="id" class="py-24 border-b border-slate-200 dark:border-slate-800 scroll-mt-20">
    <div class="max-w-[1400px] mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <div class="inline-flex items-center justify-center p-2 rounded-xl bg-slate-100 dark:bg-slate-800 text-brand-blue mb-4">
          <component :is="icon" class="w-6 h-6" v-if="icon" />
          <span class="ml-2 text-sm font-semibold uppercase tracking-wider text-slate-500 dark:text-slate-400">Capítulo {{ chapter }}</span>
        </div>
        <h2 class="text-4xl font-bold text-slate-900 dark:text-white mb-4">{{ title }}</h2>
        <p class="text-xl text-slate-600 dark:text-slate-400 max-w-3xl mx-auto">{{ subtitle }}</p>
      </div>
      <slot></slot>
    </div>
  </section>
</template>
