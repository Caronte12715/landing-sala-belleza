<script setup>
const team = [
  {
    name: 'Isabella M.',
    role: 'Directora Creativa',
    image: 'https://images.unsplash.com/photo-1595959183082-7b570b7e08e2?q=80&w=600&auto=format&fit=crop'
  },
  {
    name: 'Sofía R.',
    role: 'Especialista en Color',
    image: 'https://images.unsplash.com/photo-1607746882042-944635dfe10e?q=80&w=600&auto=format&fit=crop'
  },
  {
    name: 'Elena G.',
    role: 'Estilista Senior',
    image: 'https://images.unsplash.com/photo-1580618672591-eb180b1a973f?q=80&w=600&auto=format&fit=crop'
  }
];
</script>

<template>
  <section id="equipo" class="py-32 bg-salon-light relative">
    <div class="max-w-7xl mx-auto px-6">
      
      <div class="text-center mb-20 reveal-up">
        <span class="text-salon-primary font-sans font-medium tracking-[0.3em] uppercase text-xs mb-4 block">
          Las Artistas
        </span>
        <h2 class="font-serif text-5xl md:text-6xl text-salon-dark">Conoce a las <span class="italic font-light text-salon-primary">Creadoras</span></h2>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
        <div 
          v-for="(member, index) in team" 
          :key="index"
          class="flex flex-col items-center group cursor-pointer reveal-up"
          :class="`delay-${(index + 1) * 100}`"
        >
          <div class="w-64 h-64 md:w-72 md:h-72 rounded-full overflow-hidden mb-8 relative shadow-xl shadow-salon-dark/5 p-2 border border-salon-primary/20 group-hover:border-salon-primary transition-colors duration-500">
            <div class="w-full h-full rounded-full overflow-hidden relative">
              <div class="absolute inset-0 bg-salon-primary/10 mix-blend-multiply group-hover:opacity-0 transition-opacity duration-500 z-10 pointer-events-none"></div>
              <img :src="member.image" :alt="member.name" class="w-full h-full object-cover transform scale-105 group-hover:scale-100 transition-transform duration-700" />
            </div>
          </div>
          <h3 class="font-serif text-3xl text-salon-dark mb-2 group-hover:text-salon-primary transition-colors">{{ member.name }}</h3>
          <p class="font-sans text-salon-dark/60 font-medium tracking-[0.2em] uppercase text-xs">{{ member.role }}</p>
        </div>
      </div>
      
    </div>
  </section>
</template>
