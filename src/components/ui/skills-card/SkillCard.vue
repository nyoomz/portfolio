<script setup lang="ts">
import type { HTMLAttributes } from "vue"
import { cn } from "@/lib/utils"

const props = defineProps<{
  class?: HTMLAttributes["class"]
  title?: string
  icon?: string
}>()
</script>

<template>
  <div
    :class="cn(
      'flex items-center justify-center w-full aspect-[2/1] p-4 rounded-2xl border shadow-sm hover:scale-105 transition-transform',
      $props.class
    )"
  >
    <img
      :src="icon"
      :alt="title"
      class="w-16 h-16 md:w-20 md:h-20 object-contain"
    />  
  </div>
</template>
