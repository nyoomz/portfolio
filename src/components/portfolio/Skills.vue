<script setup lang="ts">
import SkillCard from '@/components/ui/skills-card/SkillCard.vue'
import htmlIcon from '@/assets/html.webp'
import cssIcon from '@/assets/css.png'
import jsIcon from '@/assets/js.webp'
import phpIcon from '@/assets/php.png'
import vueIcon from '@/assets/vue.png'
import laravelIcon from '@/assets/laravel.png'
import mysqlIcon from '@/assets/mysql.png'
import vscodeIcon from '@/assets/vscode.png'
import figmaIcon from '@/assets/figma.png'
import bootstrapIcon from '@/assets/bootstrap.png'
import tailwindIcon from '@/assets/tailwind.png'

const SkillCardDetails = [
    { title: 'HTML', src: htmlIcon },
    { title: 'CSS', src: cssIcon },
    { title: 'JS', src: jsIcon },
    { title: 'PHP', src: phpIcon },
    { title: 'Laravel', src: laravelIcon },
    { title: 'Vue', src: vueIcon },
    { title: 'Tailwind', src: tailwindIcon },
    { title: 'MySQL', src: mysqlIcon },
    { title: 'Figma', src: figmaIcon },
    { title: 'VS Code', src: vscodeIcon },
];

</script>

<template>
    <section id="skills" class="min-h-screen py-20 px-4 bg-card">
        <div class="container max-w-6xl mx-auto">
            <div class="mb-16">
                <p class="text-base md:text-lg text-muted-foreground leading-relaxed">
                    I’m a <span class="font-bold text-foreground">4th year BS Information Technology student</span> from Central Luzon State University with a strong interest in both design and development.
                    I enjoy breaking down complex ideas into simple, intuitive interfaces and building applications that genuinely help people. 
                    Whether I’m designing in Figma or developing with modern web tools, I focus on clarity, usability, and purposeful design.
                </p>
            </div>
            <div class="flex items-center gap-4 my-12">
                <h2 class="text-2xl md:text-3xl font-bold text-primary">
                    My Skills
                </h2>
            </div>
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-6">
                <SkillCard
                    v-for="detail in SkillCardDetails"
                    :key="detail.title"
                    :title="detail.title"
                    :icon="detail.src"
                />
            </div>
        </div>
    </section>
</template>