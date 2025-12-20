<script setup lang="ts">
import TimelineCard from "@/components/ui/timeline-card/TimelineCard.vue"

const experiences = [{
    id: 1,
    position: "Software Developer Intern",
    institution: "Department of Science and Technology",
    period: "June 2025 - July 2025",
    bullets: [
        "Developed core backend features and optimized analytics reporting for an internal government platform using Laravel, PHP, and MySQL",
        "Built and integrated data-driven modules, including scientist profiles, user/account management, and admin dashboards, to support detailed operational analysis.",
        "Improved system reliability through clean code practices, structured data workflows, and consistent backend architecture.",
    ],
},
{
    id: 2,
    position: "BS Information Technology",
    institution: "Central Luzon State University",
    period: "August 2022 - Present",
    bullets: [
        "Specializing in web development, software engineering, and database management systems.",
        "DOST Undergraduate Scholar maintaining a GPA within the range of 1.00 to 1.50 while actively participating in student organizations.",
    ]
}];
</script>

<template>
    <section id="timeline" class="py-20 px-4">
        <div class="w-full mx-auto max-w-6xl">
            <div class="flex items-center gap-4 mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-foreground">
                    Timeline
                </h2>
            </div>
            <div class="relative space-y-8">
                <div class="absolute left-1/2 transform -translate-x-1/2 w-0.5 h-full bg-primary/30 hidden md:block" />
                <div v-for="experience in experiences" :key="experience.id" 
                    class="relative flex flex-col md:flex-row items-center w-full">
                    
                    <div class="w-full md:w-1/2 flex justify-end md:pr-8">
                        <div v-if="experience.id % 2 !== 0" class="w-full">
                            <TimelineCard 
                                v-bind="experience"
                            />
                        </div>
                    </div>

                    <div class="absolute left-1/2 transform -translate-x-1/2 w-4 h-4 bg-primary rounded-full border-4 border-background hidden md:block" />

                    <div class="w-full md:w-1/2 flex justify-start md:pl-8">
                        <div v-if="experience.id % 2 === 0" class="w-full">
                            <TimelineCard 
                                v-bind="experience"
                            />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>