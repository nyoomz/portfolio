<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue"
import { Menu, X } from "lucide-vue-next"
import resumeUrl from '/Resume_Cabayao-Leah.pdf'

const navItems = [
  { label: "About", href: "#about" },
  { label: "Timeline", href: "#timeline" },
  { label: "Projects", href: "#projects" },
]

const isScrolled = ref(false)
const isMobileMenuOpen = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

onMounted(() => {
  window.addEventListener("scroll", handleScroll)
})

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll)
})
</script>

<template>
    <nav
        class="sticky top-0 inset-x-0 z-50 transition-all duration-300"
        :class="isScrolled
        ? 'bg-card/90 backdrop-blur-md shadow-soft'
        : 'bg-transparent'"
    >

        <div class="w-full mx-auto max-w-6xl">
        <div class="flex items-center justify-between h-16 md:h-20">
            
            <a href="#" class="text-xl font-bold text-foreground">
            L<span class="text-primary">M</span>C
            </a>

            <!-- desktop Navigation -->
            <div class="hidden md:flex items-center gap-8">
            <a
                v-for="item in navItems"
                :key="item.label"
                :href="item.href"
                class="text-muted-foreground hover:text-primary transition-colors font-medium text-md"
            >
                {{ item.label }}
            </a>

            <a
                :href="resumeUrl"
                download="Resume_Cabayao-Leah.pdf"
                class="px-5 py-2 rounded-full bg-blue-400 text-white text-sm font-bold hover:opacity-90 transition-opacity shadow-soft"
            >
                Download Resume
            </a>
            </div>

            <!-- Mobile Menu Button -->
            <button
            class="md:hidden w-10 h-10 flex items-center justify-center text-foreground"
            @click="isMobileMenuOpen = !isMobileMenuOpen"
            >
            <Menu v-if="!isMobileMenuOpen" class="w-6 h-6" />
            <X v-else class="w-6 h-6" />
            </button>
        </div>

        <!-- Mobile Menu -->
        <div
            v-if="isMobileMenuOpen"
            class="md:hidden absolute top-full left-0 right-0 bg-card/95 backdrop-blur-md border-t border-border shadow-card"
        >
            <div class="flex flex-col py-4">
            <a
                v-for="item in navItems"
                :key="item.label"
                :href="item.href"
                class="px-4 py-3 text-muted-foreground hover:text-primary hover:bg-muted transition-colors font-medium"
                @click="isMobileMenuOpen = false"
            >
                {{ item.label }}
            </a>

            <div class="px-4 pt-4">
                <a
                    :href="resumeUrl"
                    download="Resume_Cabayao-Leah.pdf"
                    class="px-5 py-2 rounded-full bg-blue-400 text-white text-sm font-bold hover:opacity-90 transition-opacity shadow-soft"
                >
                    Download Resume
                </a>
            </div>
            </div>
        </div>
        </div>
    </nav>
</template>