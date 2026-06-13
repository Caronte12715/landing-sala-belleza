<template>
  <section id="equipo" class="py-24 relative overflow-hidden bg-[#0A000A]">
    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-playfair text-white mb-4">Artistas de la <span class="text-transparent bg-clip-text bg-gradient-to-r from-rose-400 to-pink-300">Belleza</span></h2>
        <p class="text-rose-100/70 font-light">Conoce al equipo de profesionales detrás de cada transformación.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
        <div v-for="(member, idx) in team" :key="idx" class="group text-center">
          <div class="relative w-48 h-48 mx-auto mb-6 rounded-full overflow-hidden border-4 border-rose-500/20 group-hover:border-rose-400 transition-colors duration-500">
            <img :src="member.image" :alt="member.name" class="w-full h-full object-cover grayscale group-hover:grayscale-0 transition-all duration-500 transform group-hover:scale-110" />
          </div>
          <h3 class="text-xl font-bold text-white mb-1">{{ member.name }}</h3>
          <p class="text-rose-300 text-sm mb-3">{{ member.role }}</p>
          <p class="text-gray-400 text-sm font-light px-4">{{ member.bio }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const team = [
  { name: 'Elena Torres', role: 'Directora Creativa / Colorista', bio: 'Especialista en rubios y corrección de color con 10 años de experiencia.', image: 'https://images.unsplash.com/photo-1595959183082-7b570b7e08e2?auto=format&fit=crop&q=80&w=400' },
  { name: 'Laura Gómez', role: 'Hair Stylist', bio: 'Experta en cortes de vanguardia y tratamientos de recuperación capilar.', image: 'https://images.unsplash.com/photo-1580618672591-eb180b1a973f?auto=format&fit=crop&q=80&w=400' },
  { name: 'Ana Martínez', role: 'Makeup Artist', bio: 'Maquilladora profesional especializada en novias y eventos de gala.', image: 'https://images.unsplash.com/photo-1516975080661-46bfa2c22401?auto=format&fit=crop&q=80&w=400' }
];
</script>
