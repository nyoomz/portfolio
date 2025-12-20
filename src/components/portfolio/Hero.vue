<script setup lang="ts">
import profile from '@/assets/profile.png'
import { Mail, Phone, MapPin, Linkedin, Github } from 'lucide-vue-next'
</script>

<template>
    <section id="about" class="min-h-screen flex items-center justify-center py-20 px-2 relative overflow-hidden">    
        <div class="container max-w-6xl relative z-10">
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
                <div class="text-center md:text-left order-2 md:order-2 space-y-6">
                    <h1 class="text-2l md:text-4xl lg:text-6xl font-medium text-foreground">Hello! I'm <span class="font-bold text-primary">Leah Cabayao</span></h1>
                    <p class="text-lg">A detail-oriented and driven student pursuing a degree in 
                        <span class="font-bold">BS Information Technology</span> at the Central Luzon State University.
                        Passionate about creating impactful digital solutions that address real challenges.
                    </p>

                    <div class="space-y-2 mt-6">
                        <div class="flex items-center gap-8">
                            <div class="w-10 h-10 bg-blue-200 rounded-full flex items-center justify-center ">
                                <Mail class="text-blue-600 w-5 h-5" />
                            </div>
                            <p>leahm.cabayao@gmail.com</p>
                        </div>
                        <div class="flex items-center gap-6">
                            <div class="w-10 h-10 bg-blue-200 rounded-full flex items-center justify-center">
                                <Phone class="text-blue-600 w-5 h-5" />
                            </div>
                            <p>+63 929 711 2114</p>
                        </div>
                        <div class="flex items-center gap-6">
                            <div class="w-10 h-10 bg-blue-200 rounded-full flex items-center justify-center">
                                <MapPin class="text-blue-600 w-5 h-5" />
                            </div>
                            <p>Olongapo City, Zambales, 2200</p>
                        </div>
                    </div>

                    <div class="flex gap-4 justify-center md:justify-start animate-fade-in-up">
                    <a 
                        href="https://www.linkedin.com/in/leah-cabayao/" 
                        class="w-12 h-12 bg-primary text-primary-foreground rounded-full flex items-center justify-center hover:scale-110 transition-transform shadow-soft"
                    >
                        <Linkedin class="w-5 h-5" />
                    </a>
                    <a 
                        href="https://github.com/nyoomz" 
                        class="w-12 h-12 bg-primary text-primary-foreground rounded-full flex items-center justify-center hover:scale-110 transition-transform shadow-soft"
                    >
                        <Github class="w-5 h-5" />
                    </a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>