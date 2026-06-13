<script setup>
</script>

<template>
  <section class="relative h-screen min-h-[600px] flex items-center justify-center overflow-hidden">
    <!-- Background Image -->
    <div class="absolute inset-0 z-0">
      <img src="/images/hero.png" alt="Interior Elegance Salon" class="w-full h-full object-cover object-center" />
      <div class="absolute inset-0 bg-salon-dark/40 mix-blend-multiply"></div>
      <div class="absolute inset-0 bg-gradient-to-t from-salon-light via-transparent to-transparent opacity-80"></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 text-center px-4 max-w-4xl mx-auto mt-16 animate-fade-in-up">
      <span class="text-salon-accent font-semibold tracking-[0.2em] uppercase text-sm md:text-base mb-6 block">
        Bienvenidos a la experiencia definitiva
      </span>
      <h1 class="text-5xl md:text-7xl lg:text-8xl text-white mb-8 leading-tight drop-shadow-md">
        Realza tu belleza <br/>
        <span class="italic text-salon-secondary font-light">natural</span>
      </h1>
      <p class="text-salon-light/90 text-lg md:text-xl font-light mb-12 max-w-2xl mx-auto drop-shadow">
        Descubre un oasis de relajación y estilo. Nuestros expertos están listos para transformar tu imagen con técnicas de vanguardia y productos premium.
      </p>
      
      <div class="flex flex-col sm:flex-row items-center justify-center gap-6">
        <a href="#reservar" class="w-full sm:w-auto bg-salon-primary hover:bg-yellow-600 text-white px-10 py-4 rounded-none font-bold text-sm transition-all duration-300 uppercase tracking-widest hover:-translate-y-1">
          Agendar Cita
        </a>
        <a href="#servicios" class="w-full sm:w-auto bg-transparent border-2 border-white hover:bg-white hover:text-salon-dark text-white px-10 py-4 rounded-none font-bold text-sm transition-all duration-300 uppercase tracking-widest hover:-translate-y-1">
          Ver Servicios
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in-up {
  animation: fadeInUp 1s ease-out forwards;
}
</style>
