<template>
  <section id="testimonios" class="py-24 relative overflow-hidden bg-[#1E0B16]">
    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-playfair text-white mb-4">Experiencias <span class="text-transparent bg-clip-text bg-gradient-to-r from-rose-400 to-pink-300">Elegance</span></h2>
        <p class="text-rose-100/70 font-light">Lo que dicen nuestras clientas sobre su transformación.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div v-for="(review, idx) in reviews" :key="idx" class="bg-white/5 backdrop-blur-xl border border-white/10 p-8 rounded-2xl hover:border-rose-400/30 transition-all duration-300 hover:-translate-y-2">
          <div class="flex items-center gap-2 mb-4 text-rose-400">
            <svg v-for="i in 5" :key="i" class="w-5 h-5 fill-current" viewBox="0 0 20 20"><path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/></svg>
          </div>
          <p class="text-gray-300 italic mb-6 text-sm leading-relaxed">"{{ review.text }}"</p>
          <div class="flex items-center gap-4">
            <div class="w-12 h-12 rounded-full bg-rose-500/20 overflow-hidden border border-rose-500/30">
               <img :src="review.avatar" alt="Avatar" class="w-full h-full object-cover" />
            </div>
            <div>
              <h4 class="text-white font-medium">{{ review.name }}</h4>
              <span class="text-rose-200/60 text-xs">{{ review.service }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const reviews = [
  { name: 'Valentina R.', service: 'Balayage & Corte', text: 'Increíble la atención al detalle. Mi cabello nunca se había visto tan sano después de una decoloración. Las mejores.', avatar: 'https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&q=80&w=150' },
  { name: 'Sofía M.', service: 'Maquillaje de Novia', text: 'Me hicieron sentir como una reina el día de mi boda. El maquillaje duró intacto toda la noche. Recomendadas 100%.', avatar: 'https://images.unsplash.com/photo-1438761681033-6461ffad8d80?auto=format&fit=crop&q=80&w=150' },
  { name: 'Camila T.', service: 'Tratamiento Capilar', text: 'El ambiente del salón es un lujo. Me relajé muchísimo y mi cabello quedó suave y brillante. Ya agendé mi próxima cita.', avatar: 'https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&q=80&w=150' }
];
</script>
