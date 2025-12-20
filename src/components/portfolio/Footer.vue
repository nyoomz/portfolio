<script setup lang="ts">

const currentYear = new Date().getFullYear();

</script>

<template>
    <footer class="py-8 px-4 bg-foreground">
     <div class="w-full mx-auto max-w-6xl">
        <div class="flex flex-col md:flex-row items-center justify-end gap-4">
          <p class="text-muted text-sm">
            © {{ currentYear }} All rights reserved.
          </p>
        </div>
      </div>
    </footer>
</template>