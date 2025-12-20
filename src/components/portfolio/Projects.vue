<script setup lang="ts">
import { Card, CardTitle, CardDescription } from '@/components/ui/card'
import iMove from '@/assets/iMOVE.png'
import iskonnect from '@/assets/iskonnect.png'
import kwentoKwela from '@/assets/kwentoKwela.png'

const projects = [
    {
        title: 'International Mobility Oversight and Visitor Engagement System',
        description: 'A centralized mobility management platform that streamlines student records, compliance, and international engagement. It leverages data-driven analytics to help institutions track and optimize global exchange performance.',
        imageSrc: iMove,
        techStacks: ['Laravel', 'PHP', 'Vue.js'],
    },
    {
        title: 'Iskonnect',
        description: 'An all-in-one scholarship management system connecting applicants and administrators. It simplifies the end-to-end process—from application to document tracking—increasing transparency and accessibility for students.',
        imageSrc: iskonnect,
        techStacks: ['Laravel', 'PHP'],
    },
    {
        title: 'Kwento Kwela',
        description: 'An interactive child-friendly platform promoting Filipino culture through digital storytelling. It combines engaging narratives and visuals with early learning activities to make reading culturally rooted and fun.',
        imageSrc: kwentoKwela,
        techStacks: ['Figma'],
        
    },
]

</script>

<template>
    <section id="projects" class="py-20 px-4 bg-card">
        <div class="w-full mx-auto max-w-6xl">
            <div class="flex items-center gap-4 mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-foreground">
                    Projects
                </h2>
            </div>
            <div class="space-y-4">
                <Card class="grid md:grid-cols-2 p-6 border" v-for="project in projects" :key="project.title">
                    <div >
                       <img :src="project.imageSrc" :alt="project.title" class="w-full h-auto rounded-lg hover:scale-105 transition-transform shadow-sm"/> 
                    </div>
                    <div>
                        <CardTitle class="text-2xl mb-3">{{ project.title }}</CardTitle>
                        <CardDescription class="text-md text-gray-700">{{ project.description }}</CardDescription>
                        <div class="inline-block rounded-xl py-1 px-4 me-2 mt-2 text-sm font-medium bg-blue-300" v-for="techStack in project.techStacks">
                            {{ techStack }}
                        </div>
                    </div>
                </Card>
            </div>
        </div>

       
    </section>
    
</template>