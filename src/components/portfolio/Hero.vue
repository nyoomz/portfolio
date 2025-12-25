<script setup lang="ts">
import profile from '@/assets/profile.jpg'
import { Mail, Phone, MapPin, Linkedin, Github } from 'lucide-vue-next'
</script>

<template>
    <section id="about" class="min-h-screen flex items-center justify-center py-20 px-2 relative overflow-hidden">    
        <div class="container max-w-6xl relative z-10 px-4">
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="flex justify-center sn:justify-end order-1 md:order-1">
                    <div class="relative">
                        <div class="absolute inset-0 -m-4 border-4 border-primary/20 rounded-full animate-pulse" />
                        <div class="absolute -top-2 -right-2 w-8 h-8 bg-primary rounded-full" />
                        <div class="absolute -bottom-4 -left-4 w-12 h-12 border-4 border-primary rounded-full" />

                        <div class="w-64 h-64 md:w-80 md:h-80 rounded-full overflow-hidden border-8">
                            <img 
                                :src="profile"
                                alt="Leah Cabayao" 
                                class="w-full h-full object-cover"
                            />
                        </div>
                    </div>
                </div>
                <div class="text-left order-2 md:order-2 space-y-4">
                    <p class="text-sm md:text-base font-medium text-foreground">Hello! My name is</p>
                    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-primary leading-tight">Leah Cabayao</h1>
                    <p class="text-sm md:text-base text-muted-foreground max-w-xl leading-relaxed">
                        A driven and detail-oriented IT student interested in building 
                        <span class="font-bold text-foreground">clear, user-centered digital solutions</span> 
                        that solve real-world problems.
                    </p>

                    <div class="space-y-3 pt-2">
                        <div class="flex items-center gap-4">
                            <div class="w-10 h-10 bg-blue-200 rounded-full flex items-center justify-center shrink-0">
                                <Mail class="text-blue-600 w-5 h-5" />
                            </div>
                            <p class="text-sm md:text-base text-foreground">leahm.cabayao@gmail.com</p>
                        </div>
                        <div class="flex items-center gap-4">
                            <div class="w-10 h-10 bg-blue-200 rounded-full flex items-center justify-center shrink-0">
                                <Phone class="text-blue-600 w-5 h-5" />
                            </div>
                            <p class="text-sm md:text-base text-foreground">+63 929 711 2114</p>
                        </div>
                        <div class="flex items-center gap-4">
                            <div class="w-10 h-10 bg-blue-200 rounded-full flex items-center justify-center shrink-0">
                                <MapPin class="text-blue-600 w-5 h-5" />
                            </div>
                            <p class="text-sm md:text-base text-foreground">Olongapo City, Zambales, 2200</p>
                        </div>
                    </div>

                    <div class="flex gap-4 justify-start pt-2">
                    <a 
                        href="https://www.linkedin.com/in/leah-cabayao/" 
                        target="_blank"
                        rel="noopener noreferrer"
                        class="w-12 h-12 bg-primary text-primary-foreground rounded-full flex items-center justify-center hover:scale-110 transition-transform shadow-soft"
                        aria-label="LinkedIn Profile"
                    >
                        <Linkedin class="w-5 h-5" />
                    </a>
                    <a 
                        href="https://github.com/nyoomz" 
                        target="_blank"
                        rel="noopener noreferrer"
                        class="w-12 h-12 bg-primary text-primary-foreground rounded-full flex items-center justify-center hover:scale-110 transition-transform shadow-soft"
                        aria-label="GitHub Profile"
                    >
                        <Github class="w-5 h-5" />
                    </a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>