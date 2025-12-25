<script setup lang="ts">
import { Card, CardTitle, CardDescription } from '@/components/ui/card'
import iMove from '@/assets/iMOVE.jpg'
import iskonnect from '@/assets/iskonnect.jpg'
import kwentoKwela from '@/assets/kwentoKwela.png'

const projects = [
    {
        title: 'International Mobility Oversight and Visitor Engagement System',
        description: 'A centralized mobility management platform that streamlines student records, compliance, and international engagement. It leverages data-driven analytics to help institutions track and optimize global exchange performance.',
        imageSrc: iMove,
        techStacks: ['Laravel', 'PHP', 'Vue.js'],
        notes: 'Launching soon. Check out the current demo video for the meantime!',
        link: 'https://youtu.be/nzBMv93Sdmc',
    },
    {
        title: 'Iskonnect',
        description: 'An all-in-one scholarship management system connecting applicants and administrators. It simplifies the end-to-end process—from application to document tracking—increasing transparency and accessibility for students.',
        imageSrc: iskonnect,
        techStacks: ['Laravel', 'PHP'],
        notes: 'Source code available!',
        link: 'https://github.com/nyoomz/iskonnect-laravel'
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
        <div class="container max-w-6xl mx-auto">
            <div class="flex items-center gap-4 mb-12">
                <h2 class="text-2xl md:text-3xl font-bold text-primary">
                    Projects
                </h2>
            </div>
            <div class="space-y-8">
                <Card class="grid md:grid-cols-[2fr_1fr] p-6 shadow-none border border-border" v-for="project in projects" :key="project.title">
                    <div >
                       <img :src="project.imageSrc" :alt="project.title" class="w-full h-auto rounded-lg hover:scale-102 transition-transform"/> 
                    </div>
                    <div class="flex flex-col h-full lg:ps-6 mt-4 md:mt-0">
                        <div class="flex-1 space-y-4">
                            <CardTitle class="text-2xl font-bold text-foreground mb-3">{{ project.title }}</CardTitle>
                            <CardDescription class="text-sm text-muted-foreground leading-relaxed">{{ project.description }}</CardDescription>
                            <div class="inline-block rounded-full py-1 px-3 me-2 text-sm font-medium bg-blue-300" v-for="techStack in project.techStacks" :key="techStack">
                                {{ techStack }}
                            </div>
                        </div>
                        <p v-if="project.notes" class="mt-6 text-sm text-muted-foreground italic">
                            * {{ project.notes }}
                        <a
                            v-if="project.link"
                            :href="project.link"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="font-medium text-primary underline underline-offset-2"
                        >
                            Link
                        </a>
                        </p>
                    </div>
                </Card>
            </div>
        </div>

       
    </section>
    
</template>