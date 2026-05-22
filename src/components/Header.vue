<script setup>
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
                        
                  <div class="text-white text-3xl font-black cursor-pointer">
                        PORTAFOLIO
                        <span class="text-primary">.</span>
                  </div>

                  <nav></nav>

                  </div>
            </header>
      </div>
</template>


