<script setup lang="ts">
import { ref, onMounted } from 'vue'
import Navigation from '@/components/portfolio/Navigation.vue'
import Hero from '@/components/portfolio/Hero.vue'
import Skills from '@/components/portfolio/Skills.vue'
import Experience from '@/components/portfolio/Timeline.vue'
import Projects from './components/portfolio/Projects.vue'
import Footer from '@/components/portfolio/Footer.vue'
import LoadingScreen from '@/components/ui/LoadingScreen.vue'

const isLoading = ref(true)
const minLoadingTime = 1000 
const preloadImages = async () => {
  const startTime = Date.now()
  
  const imagesToLoad = [
    '/src/assets/profile.jpg',
    '/src/assets/html.webp',
    '/src/assets/css.png',
    '/src/assets/js.webp',
    '/src/assets/php.png',
    '/src/assets/vue.png',
    '/src/assets/laravel.png',
    '/src/assets/mysql.png',
    '/src/assets/vscode.png',
    '/src/assets/figma.png',
    '/src/assets/bootstrap.png',
    '/src/assets/tailwind.png',
    '/src/assets/iMOVE.jpg',
    '/src/assets/iskonnect.jpg',
    '/src/assets/kwentoKwela.png',
  ]

  const imagePromises = imagesToLoad.map((src) => {
    return new Promise((resolve) => {
      const img = new Image()
      img.src = src
      img.onload = resolve
      img.onerror = resolve
    })
  })

  await Promise.all(imagePromises)
  
  const elapsedTime = Date.now() - startTime
  if (elapsedTime < minLoadingTime) {
    await new Promise(resolve => setTimeout(resolve, minLoadingTime - elapsedTime))
  }
  
  isLoading.value = false
}

onMounted(() => {
  preloadImages()
})
</script>

<template>
  <LoadingScreen :is-loading="isLoading" />
  <Transition
    enter-active-class="transition-opacity duration-500 ease-in-out"
    enter-from-class="opacity-0"
    enter-to-class="opacity-100"
  >
    <main v-show="!isLoading" class="min-h-screen">
      <Navigation />
      <Hero />
      <Skills />
      <Experience />
      <Projects />
      <Footer />
    </main>
  </Transition>
</template>