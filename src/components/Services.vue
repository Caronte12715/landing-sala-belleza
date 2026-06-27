<script setup>
const services = [
  {
    title: 'Corte y Estilo',
    description: 'Asesoría de imagen y cortes de tendencia adaptados a tu estructura facial.',
    price: 'Desde $45',
    image: 'https://images.unsplash.com/photo-1595476108010-b4d1f10d5e43?q=80&w=800&auto=format&fit=crop'
  },
  {
    title: 'Coloración Premium',
    description: 'Balayage, babylights y técnicas de color con productos orgánicos sin amoníaco.',
    price: 'Desde $120',
    image: 'https://images.unsplash.com/photo-1521590832167-7bfc17484d56?q=80&w=800&auto=format&fit=crop'
  },
  {
    title: 'Tratamientos Capilares',
    description: 'Botox capilar, queratina y reconstrucción profunda para devolver la vida a tu cabello.',
    price: 'Desde $85',
    image: 'https://images.unsplash.com/photo-1560066984-138dadb4c035?q=80&w=800&auto=format&fit=crop'
  },
  {
    title: 'Maquillaje Social',
    description: 'Maquillaje profesional para eventos, novias y editoriales con acabado impecable.',
    price: 'Desde $75',
    image: 'https://images.unsplash.com/photo-1512496015851-a1c8ca9d7f5c?q=80&w=800&auto=format&fit=crop'
  }
];
</script>

<template>
  <section id="servicios" class="py-32 bg-salon-light relative">
    <div class="max-w-7xl mx-auto px-6">
      
      <div class="text-center max-w-2xl mx-auto mb-20 reveal-up">
        <h2 class="font-serif text-5xl md:text-6xl text-salon-dark mb-6">Nuestros <span class="italic font-light text-salon-primary">Servicios</span></h2>
        <p class="font-sans text-salon-dark/70 font-light text-lg">
          Experiencias diseñadas para realzar tu belleza natural con productos botánicos y técnicas de vanguardia.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-10 lg:gap-16">
        <div 
          v-for="(service, index) in services" 
          :key="index"
          class="group relative bg-white p-8 md:p-12 rounded-2xl shadow-sm hover:shadow-2xl hover:-translate-y-2 transition-all duration-500 reveal-up"
          :class="`delay-${(index + 1) * 100}`"
        >
          <!-- Imagen Revelada en Hover -->
          <div class="absolute inset-0 rounded-2xl overflow-hidden opacity-0 group-hover:opacity-10 transition-opacity duration-700 pointer-events-none">
            <img :src="service.image" alt="" class="w-full h-full object-cover filter grayscale" />
          </div>
          
          <div class="relative z-10">
            <div class="flex justify-between items-start mb-6">
              <h3 class="font-serif text-3xl text-salon-dark group-hover:text-salon-primary transition-colors duration-300">{{ service.title }}</h3>
              <span class="font-sans text-salon-accent font-medium tracking-wider">{{ service.price }}</span>
            </div>
            <p class="font-sans text-salon-dark/60 font-light leading-relaxed mb-8">
              {{ service.description }}
            </p>
            <a href="#cita" class="inline-flex items-center gap-2 font-sans text-xs font-semibold tracking-[0.2em] uppercase text-salon-dark group-hover:text-salon-primary transition-colors">
              Reservar
              <svg class="w-4 h-4 transform group-hover:translate-x-2 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17 8l4 4m0 0l-4 4m4-4H3" />
              </svg>
            </a>
          </div>
        </div>
      </div>
      
    </div>
  </section>
</template>
