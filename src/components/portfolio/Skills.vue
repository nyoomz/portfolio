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
    { title: 'Bootstrap', src: bootstrapIcon },
    { title: 'MySQL', src: mysqlIcon },
    { title: 'Figma', src: figmaIcon },
    { title: 'VS Code', src: vscodeIcon },
];

</script>

<template>
    <section class="py-20 bg-card">
        <div class="w-full mx-auto max-w-6xl">
            <div class="flex items-center gap-4 mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-foreground">
                    Skills
                </h2>
            </div>
            <div class="flex flex-wrap items-center justify-center gap-6">
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