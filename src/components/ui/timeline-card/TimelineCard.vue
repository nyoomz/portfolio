<script setup lang="ts">
import { Card, CardTitle, CardDescription } from '@/components/ui/card'

defineProps<{
    position: string;
    institution: string;
    period: string;
    bullets: string[];
}>()

</script>

<template>
    <Card class="p-6 mt-4 rounded-lg shadow-md border-primary">
        <div>
            <CardTitle class="text-2xl font-bold text-foreground ">
                {{ position }}
            </CardTitle>
            <CardDescription class="text-primary font-semibold text-lg mb-4">{{ institution }}</CardDescription>
            <CardDescription class="text-gray-500 font-semibold text-md mb-4">{{ period }}</CardDescription>
            <ul class="space-y-2" v-for="bullet in bullets" :key="bullet">
                <li class="text-muted-foreground text-md leading-relaxed flex gap-2">
                    <span class="text-primary shrink-0">•</span>
                    {{ bullet }}
                </li>
            </ul>
        </div>
    </Card>
</template>
