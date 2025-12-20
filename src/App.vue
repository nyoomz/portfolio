<script setup lang="ts">
import Navigation from '@/components/portfolio/Navigation.vue';
import Hero from '@/components/portfolio/Hero.vue';
import Skills from '@/components/portfolio/Skills.vue';
import Experience from '@/components/portfolio/Timeline.vue';
import Projects from './components/portfolio/Projects.vue';
import Footer from '@/components/portfolio/Footer.vue';
</script>

<template>
  <main class="min-h-screen">
    <Navigation />
    <Hero />
    <Skills/>
    <Experience />
    <Projects />
    <Footer />
  </main>
</template>

<style scoped></style>
