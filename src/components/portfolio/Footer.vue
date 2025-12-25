<script setup lang="ts">

const currentYear = new Date().getFullYear();

</script>

<template>
    <footer class="py-8 px-4 bg-foreground">
     <div class="container max-w-6xl mx-auto">
        <div class="flex flex-col md:flex-row items-center justify-end gap-4">
          <p class="text-muted-foreground text-sm">
            Made in Vue.js by yours truly :D &#x2022;
            © {{ currentYear }} All rights reserved.
          </p>
        </div>
      </div>
    </footer>
</template>