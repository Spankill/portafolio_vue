<script setup>
import Header from './components/Header.vue';
import HeroSection from './components/HeroSection.vue';
import AOS from 'aos';
import 'aos/dist/aos.css';
import { onMounted } from 'vue';

onMounted(() => {
  AOS.init({
    duration: 1000,
    once: false,
    offset:100,
  })
})

</script>



<template>
  <div className="bg-[#111827] min-h-screen">

    <Header></Header>
    <HeroSection></HeroSection>

  </div>
</template>
 