<script setup>
const images = [
  'https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?q=80&w=800&auto=format&fit=crop',
  'https://images.unsplash.com/photo-1562322140-8baeececf3df?q=80&w=800&auto=format&fit=crop',
  'https://images.unsplash.com/photo-1600948836101-f9ffda59d250?q=80&w=800&auto=format&fit=crop',
  'https://images.unsplash.com/photo-1599566150163-29194dcaad36?q=80&w=800&auto=format&fit=crop'
];
</script>

<template>
  <section id="galeria" class="py-32 bg-salon-secondary relative">
    <div class="max-w-7xl mx-auto px-6">
      
      <div class="flex flex-col md:flex-row justify-between items-end mb-20 reveal-up">
        <div>
          <span class="text-salon-primary font-sans font-medium tracking-[0.3em] uppercase text-xs mb-4 block">
            Nuestro Trabajo
          </span>
          <h2 class="font-serif text-5xl md:text-6xl text-salon-dark">Lookbook</h2>
        </div>
        <p class="font-sans text-salon-dark/60 font-light max-w-md mt-6 md:mt-0">
          Inspiración y resultados reales. Cada look es creado con precisión y amor por los detalles.
        </p>
      </div>

      <!-- Masonry asimétrico -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 md:gap-12 lg:gap-20">
        
        <div class="flex flex-col gap-8 md:gap-20">
          <div class="relative overflow-hidden rounded-[40px] rounded-br-sm group reveal-up aspect-[4/5]">
            <div class="absolute inset-0 bg-salon-primary/20 mix-blend-multiply group-hover:opacity-0 transition-opacity duration-700 z-10 pointer-events-none"></div>
            <img :src="images[0]" class="w-full h-full object-cover transform scale-105 group-hover:scale-100 transition-transform duration-1000" />
          </div>
          <div class="relative overflow-hidden rounded-[40px] rounded-tl-sm group reveal-up aspect-square w-3/4 ml-auto">
            <div class="absolute inset-0 bg-salon-primary/20 mix-blend-multiply group-hover:opacity-0 transition-opacity duration-700 z-10 pointer-events-none"></div>
            <img :src="images[1]" class="w-full h-full object-cover transform scale-105 group-hover:scale-100 transition-transform duration-1000" />
          </div>
        </div>

        <div class="flex flex-col gap-8 md:gap-20 md:mt-32">
          <div class="relative overflow-hidden rounded-[40px] rounded-tr-sm group reveal-up aspect-square w-4/5">
            <div class="absolute inset-0 bg-salon-primary/20 mix-blend-multiply group-hover:opacity-0 transition-opacity duration-700 z-10 pointer-events-none"></div>
            <img :src="images[2]" class="w-full h-full object-cover transform scale-105 group-hover:scale-100 transition-transform duration-1000" />
          </div>
          <div class="relative overflow-hidden rounded-[40px] rounded-bl-sm group reveal-up aspect-[3/4]">
            <div class="absolute inset-0 bg-salon-primary/20 mix-blend-multiply group-hover:opacity-0 transition-opacity duration-700 z-10 pointer-events-none"></div>
            <img :src="images[3]" class="w-full h-full object-cover transform scale-105 group-hover:scale-100 transition-transform duration-1000" />
          </div>
        </div>

      </div>
      
    </div>
  </section>
</template>
