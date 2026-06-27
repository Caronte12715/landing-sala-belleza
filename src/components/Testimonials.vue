<script setup>
const testimonials = [
  {
    name: 'Valeria C.',
    text: 'El nivel de detalle y el trato personalizado me hicieron sentir en un verdadero santuario. Mi cabello nunca había lucido tan saludable y radiante.',
  },
  {
    name: 'Andrea P.',
    text: 'Entendieron exactamente lo que quería. El color es perfecto y la experiencia en el salón fue increíblemente relajante.',
  }
];
</script>

<template>
  <section class="py-32 bg-salon-secondary relative overflow-hidden">
    <!-- Decoración de fondo -->
    <div class="absolute inset-0 flex items-center justify-center opacity-5 pointer-events-none">
      <span class="font-serif text-[30vw] text-salon-primary leading-none">A</span>
    </div>

    <div class="max-w-6xl mx-auto px-6 relative z-10">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
        
        <div class="flex flex-col justify-center reveal-left">
          <span class="text-salon-primary font-sans font-medium tracking-[0.3em] uppercase text-xs mb-4 block">
            Voces
          </span>
          <h2 class="font-serif text-5xl md:text-6xl text-salon-dark mb-8">Lo que dicen <br/><span class="italic font-light text-salon-primary">nuestras musas</span></h2>
          <div class="w-16 h-[1px] bg-salon-primary"></div>
        </div>

        <div class="flex flex-col gap-12">
          <div 
            v-for="(t, index) in testimonials" 
            :key="index"
            class="bg-white/50 backdrop-blur-sm p-10 rounded-tr-[40px] rounded-bl-[40px] border border-salon-primary/10 hover:border-salon-primary/30 transition-colors reveal-right"
            :class="`delay-${(index + 1) * 200}`"
          >
            <div class="flex text-salon-accent mb-6">
              <svg v-for="i in 5" :key="i" class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
            </div>
            <p class="font-serif text-2xl text-salon-dark leading-relaxed mb-6 italic">"{{ t.text }}"</p>
            <span class="font-sans font-medium tracking-widest text-xs uppercase text-salon-primary">{{ t.name }}</span>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
