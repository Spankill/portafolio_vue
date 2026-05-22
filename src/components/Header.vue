<script setup>
import { MenuIcon, XIcon } from '@lucide/vue';
import {ref} from 'vue';

const isMenuOpen = ref(false);

const menuItems = [
      {name: 'Education', href:'#education'},
      {name: 'Certificates', href:'#certificates'},
      {name: 'About', href:'#about'},
      {name: 'Skills', href:'#skills'},
      {name: 'Projects', href:'#projects'},
]
const scrollToSection = (href) => {
      isMenuOpen.value = false
      const element = document.querySelector(href)
      if(element){
            element.scrollIntoView({
                  behavior: 'smooth'
            })
      }
}

</script>



<template lang="">
      <div>
            <header class="relative z-50 px-6 py-7">
                  <div class="max-w-7xl mx-auto flex justify-between items-center">
                        <!-- Logo -->
                        <div class="text-white text-3xl font-black cursor-pointer">
                              PORTAFOLIO
                              <span class="text-primary">.</span>
                        </div>
                        <!-- Navegador -->
                        <nav class="hidden md:flex items-center gap-10">
                              <ul class="flex gap-8">
                                    <li v-for="item in menuItems" :key="item.name">
                                          <button 
                                          @click="scrollToSection(item.href)"
                                          class="text-gray-300 hover:text-white text-base font-medium transition-colors" >
                                          {{item.name}}
                                          </button>
                                    </li>
                              </ul>
                              <button 
                              @click="scrollToSection('#contact')" 
                              class="bg-primary hover:bg-primary/90 text-white px-6 py-2.5 rounded-lg text-base font-semibold transition-all"
                              >
                              Contact Me
                              </button>
                        </nav>
                        <!--  menu Hamburguesa -->
                        <button 
                        class="md:hidden text-white relative z-[60] p-2 focus-outline-none"
                        @click="isMenuOpen = !isMenuOpen">
                              <MenuIcon v-if="!isMenuOpen" :size="32"></MenuIcon>
                              <XIcon v-else :size="32"></XIcon>
                        </button>
                  </div> 
                  <!-- fondo oscuro -->
                  <div v-show="isMenuOpen" 
                  class="fixed inset-0 bg-black/60 ba ckdrop-blur-sm md:hidden"
                  @click="isMenuOpen = false">
                  </div>
                  <!-- menu lateral -->
                  <div 
                  class="fixed top-0 right-0 h-full w-80 bg-[#111827] p-6 z-50 transform transition-transform duration-300 md:hidden flex flex-col pt-24"
                  :class="isMenuOpen ? 'translate-x-0' : 'translate-x-full'"
                  >

                  

                  <ul class="flex flex-col gap-8">
                        <li v-for="item in menuItems" :key="item.name">
                              <button 
                              @click="scrollToSection(item.href)"
                              class="text-white text-xl font-semibold hover:text-primary transition-colors"
                              >
                              {{item.name}}
                              </button>
                        </li>
                        <li class="pt-6">
                              <button 
                              @click="scrollToSection('#contact')" 
                              class="w-full bg-primary text-white py-4 rounded-xl text-lg fon">
                              Contact Me
                              </button>
                        </li>
                  </ul>
                  </div>
            </header>
      </div>
</template>


