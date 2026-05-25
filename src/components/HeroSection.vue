<script setup> 
import { Download } from '@lucide/vue'
import hero from '../assets/heroimage.png'
</script>


<template lang="">
      <section class="relative w-full min-h-screen flex items-start py-24" data-aos="zoom-in-up">
            <!-- fondo difuminado -->
            <div class="absolute top-0 inset-x-0 h-64 flex items-start z-0">
                  <div class="h-24 w-2/3 bg-linear-to-br from-[#c3700c] blur-2xl invisible opacity-40">
                  </div>
                  <div class="h-20 w-3/4 bg-linear-to-r from-[#ff9500] opacity-60 blur-2xl">
                  </div>
            </div>
            <!-- contenido centrado -->
            <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto relative z-10">
                  <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 lg:max-w-none max-w-2xl md:max-w-3xl mx-auto">
                        <div class="lg:py-6 flex flex-col justify-center items-center lg:items-start">
                              <div class="text-center lg:text-left">
                                    <h1 class="text-white font-bold text-3xl md:text-5xl lg:text-6xl">
                                          HOLA, SOY<span class="text-transparent bg-clip-text bg-linear-to-r from-primary to-red-500 "> C@RL!TO$</span>👋🏻      
                                    </h1>
                              </div>

                              <p class="text-gray-300 pt-8 text-center lg:text-left mx-auto max-w-xl">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus dicta quos fuga quisquam dolore debitis ut maxime sed minus libero? Repellendus sapiente officiis harum laborum ullam asperiores quo nulla facilis!
                              Et magnam dolore maxime culpa, animi sit delectus sequi quas quis ipsum, dicta dignissimos repudiandae aliquam exercitationem perferendis laudantium minus nostrum! Eaque assumenda commodi perferendis.
                              </p>
                              
                              <div class="flex items-center gap-3 pt-9 flex-col sm:flex-row sm:w-max sm:mx-auto lg:mx-0">
                                    <!-- boton HIRE ME -->
                                    <button class="px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center">
                                          <span class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-primary border-2 border-transparent">
                                          </span>
                                          <span class="relative flex items-center justify-center text-white">
                                                HIRE ME
                                          </span>
                                    </button>
                                    
                                    <a href="/resume.pdf" download="resume.pdf" class="w-full sm:w-max block">
                                          
                                          <button class="border border-primary px-6 py-3 rounded-full flex items-center justify-center gap-2 group hover:bg-primary/10 transition-all duration-300 w-full sm:w-max">
                                                <!-- contenedor del icono -->
                                                <div class="flex items-center justify-center transition-transform duration-300 group-hover:scale-110">
                                                      <!-- icono -->
                                                      <Download :size="18" class="text-primary" />
                                                </div>
                                                <!-- texto -->
                                                <span class="text-primary font-medium transition-transform duration-300 group-hover:scale-105">
                                                      Download CV
                                                </span>
                                          </button>
                                    </a>
                              </div>
                        </div>
                              <!-- imagen -->
                              <div class="lg:h-full h-96 min-h-96 lg:min-h-[none] lg:w-full flex items-center justify-center lg:justify-end relative">
                                    <div class="absolute z-0 top-1/2 -translate-y-1/2 w-5/6 right-0 h-[calc(80%+20px)] bg-linear-to-tr opacity-25 from-[#0cac24] to-primary blur-2xl rounded-full">
                                    </div>
                                    <div 
                                    :style="{ borderRadius: '30% 70% 70% 30% / 30% 30% 70% 70%' }"
                                    class="relative z-10 p-2 shadow-lg border border-primary overflow-hidden max-w-100 lg:max-w-125">
                                          <img :src="hero" alt="Heroimage" 
                                          width="500" height="auto" loading="lazy"
                                          :style="{ borderRadius: '30% 70% 70% 30% / 30% 30% 70% 70%' }"
                                          class="w-full h-auto object-cover">
                                    </div>
                              </div>
                  </div>
            </div>
      </section>
</template>
