<script setup lang="ts">
import { navigateTo } from 'nuxt/app'

definePageMeta({
  layout: 'home'
})

const handleGetStarted = () => {
  navigateTo('/get-started/introduction')
    }

const handleGetStartedKeyDown = (event: KeyboardEvent) => {
  if (event.key === 'Enter') {
    event.preventDefault()
    navigateTo('/get-started/introduction')
  }
}
</script>

<template>
    <div class="min-h-screen bg-white dark:bg-stone-900 transition-colors duration-200">
        <div class="max-w-6xl mx-auto p-6">
            <div class="flex justify-end mb-8">
                <ThemeSwitcher />
            </div>

            <div class="text-center mb-16">
                <h1 class="text-5xl md:text-6xl font-bold text-stone-800 dark:text-stone-100 mb-6">
                    Doc Name <span class="text-pink-600 dark:text-pink-400">Center</span>
                </h1>
                <p class="text-xl text-stone-600 dark:text-stone-300 mb-8 max-w-2xl mx-auto">
                    Doc Name Center is a documentation center for Doc Name. It is a platform for storing and sharing documentation for Doc Name.    
                </p>
                
                <button 
                    @click="handleGetStarted"
                    @keydown="handleGetStartedKeyDown"
                    class="inline-flex items-center px-8 py-3 text-lg font-medium text-white bg-pink-600 hover:bg-pink-700 dark:bg-pink-500 dark:hover:bg-pink-600 rounded-lg transition-colors duration-200 shadow-lg hover:shadow-xl transform hover:-translate-y-1"
                    tabindex="0"
                    aria-label="Get Started"
                >
                    <span class="mr-2">🚀</span>
                    Get Started
                </button>
            </div>

            <div class="grid md:grid-cols-3 gap-8 mb-16">
                <div class="text-center p-6 bg-stone-50 dark:bg-stone-800 rounded-lg">
                    <div class="text-4xl mb-4">📚</div>
                                <h3 class="text-xl font-semibold text-stone-800 dark:text-stone-100 mb-2">Easy Navigation</h3>
            <p class="text-stone-600 dark:text-stone-300">Dynamic sidebar and table of contents for quick navigation</p>
                </div>
                <div class="text-center p-6 bg-stone-50 dark:bg-stone-800 rounded-lg">
                    <div class="text-4xl mb-4">🎨</div>
                                <h3 class="text-xl font-semibold text-stone-800 dark:text-stone-100 mb-2">Modern Design</h3>
            <p class="text-stone-600 dark:text-stone-300">Responsive and dark mode supported interface</p>
                </div>
                <div class="text-center p-6 bg-stone-50 dark:bg-stone-800 rounded-lg">
                    <div class="text-4xl mb-4">⚡</div>
                                <h3 class="text-xl font-semibold text-stone-800 dark:text-stone-100 mb-2">Quick Search</h3>
            <p class="text-stone-600 dark:text-stone-300">Quick search and filtering in content</p>
                </div>
            </div>
        </div>
    </div>
</template>
