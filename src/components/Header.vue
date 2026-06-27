<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<template>
  <header 
    class="fixed w-full top-0 z-50 transition-all duration-700"
    :class="isScrolled ? 'bg-salon-secondary/90 backdrop-blur-md py-4 shadow-sm border-b border-salon-primary/20' : 'bg-transparent py-8'"
  >
    <div class="max-w-7xl mx-auto px-6 sm:px-8 flex justify-between items-center">
      
      <!-- Logo -->
      <a href="#" class="flex flex-col items-center">
        <span class="font-serif text-3xl font-light tracking-widest text-salon-dark leading-none">A U R E A</span>
        <span class="font-sans text-[0.6rem] tracking-[0.4em] text-salon-primary uppercase mt-1">Slow Beauty</span>
      </a>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-10">
        <a href="#servicios" class="text-xs font-sans font-medium tracking-[0.2em] uppercase text-salon-dark hover:text-salon-primary transition-colors">Servicios</a>
        <a href="#galeria" class="text-xs font-sans font-medium tracking-[0.2em] uppercase text-salon-dark hover:text-salon-primary transition-colors">Lookbook</a>
        <a href="#equipo" class="text-xs font-sans font-medium tracking-[0.2em] uppercase text-salon-dark hover:text-salon-primary transition-colors">Artistas</a>
        <a href="#cita" class="text-xs font-sans font-medium tracking-[0.2em] uppercase bg-salon-dark text-salon-secondary px-8 py-3 rounded-full hover:bg-salon-primary transition-colors duration-500 shadow-lg shadow-salon-dark/10">Reservar</a>
      </nav>

      <!-- Mobile Menu Button -->
      <button class="md:hidden text-salon-dark">
        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>

    </div>
  </header>
</template>
