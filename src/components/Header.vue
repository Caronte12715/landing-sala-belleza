<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const isMobileMenuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20;
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
    :class="[
      'fixed w-full top-0 z-50 transition-all duration-300',
      isScrolled ? 'bg-white/90 backdrop-blur-md shadow-sm py-4' : 'bg-transparent py-6'
    ]"
  >
    <div class="max-w-7xl mx-auto px-6 flex justify-between items-center">
      <!-- Logo -->
      <a href="#" class="text-3xl font-serif font-bold text-salon-dark tracking-wide">
        Elegance<span class="text-salon-primary">.</span>
      </a>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-8">
        <a href="#servicios" class="text-sm font-semibold text-salon-dark hover:text-salon-primary transition-colors">Servicios</a>
        <a href="#nosotros" class="text-sm font-semibold text-salon-dark hover:text-salon-primary transition-colors">Nosotros</a>
        <a href="#galeria" class="text-sm font-semibold text-salon-dark hover:text-salon-primary transition-colors">Galería</a>
        <a href="#reservar" class="bg-salon-primary hover:bg-yellow-600 text-white px-6 py-2.5 rounded-none font-semibold text-sm transition-all duration-300 uppercase tracking-wider">
          Reservar Cita
        </a>
      </nav>

      <!-- Mobile Toggle -->
      <button 
        @click="isMobileMenuOpen = !isMobileMenuOpen" 
        class="md:hidden text-salon-dark p-2"
      >
        <svg v-if="!isMobileMenuOpen" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div 
      v-if="isMobileMenuOpen" 
      class="md:hidden absolute top-full left-0 w-full bg-white shadow-xl border-t border-gray-100 flex flex-col"
    >
      <a href="#servicios" class="p-4 border-b border-gray-50 text-center font-semibold text-salon-dark">Servicios</a>
      <a href="#nosotros" class="p-4 border-b border-gray-50 text-center font-semibold text-salon-dark">Nosotros</a>
      <a href="#galeria" class="p-4 border-b border-gray-50 text-center font-semibold text-salon-dark">Galería</a>
      <a href="#reservar" class="p-4 bg-salon-primary text-white text-center font-bold uppercase tracking-widest">Reservar Cita</a>
    </div>
  </header>
</template>
