<script setup lang="ts">
import { ref, onMounted } from 'vue'

const props = defineProps<{
  isLoading: boolean
}>()
</script>

<template>
  <Transition
    enter-active-class="transition-opacity duration-300"
    leave-active-class="transition-opacity duration-300"
    enter-from-class="opacity-100"
    enter-to-class="opacity-100"
    leave-from-class="opacity-100"
    leave-to-class="opacity-0"
  >
    <div
      v-if="isLoading"
      class="fixed inset-0 z-[100] flex items-center justify-center bg-background"
    >
      <div class="text-center space-y-4">
        <div class="relative w-16 h-16 mx-auto">
          <div class="absolute inset-0 border-4 border-primary/20 rounded-full"></div>
          <div class="absolute inset-0 border-4 border-transparent border-t-primary rounded-full animate-spin"></div>
        </div>
        <p class="text-muted-foreground font-medium">Loading...</p>
      </div>
    </div>
  </Transition>
</template>