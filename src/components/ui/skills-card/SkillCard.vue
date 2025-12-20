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
      'flex items-center justify-center w-64 h-32 p-4 rounded-2xl border shadow-sm hover:scale-105 transition-transform',
      $props.class
    )"
  >
    <img
      :src="icon"
      :alt="title"
      class="w-24 h-24 object-contain"
    />  
  </div>
</template>
