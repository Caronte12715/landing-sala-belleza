<template>
  <section id="galeria" class="py-24 relative overflow-hidden bg-[#0A000A]">
    <div class="absolute inset-0 bg-gradient-to-tr from-[#1E0B16] via-transparent to-[#1E0B16] opacity-60"></div>
    
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-playfair text-white mb-4">Nuestro <span class="text-transparent bg-clip-text bg-gradient-to-r from-rose-400 to-pink-300">Arte</span></h2>
        <p class="text-rose-100/70 max-w-2xl mx-auto font-light">Transformaciones reales que destacan la belleza única de cada uno de nuestros clientes.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div v-for="(img, idx) in gallery" :key="idx" class="group relative rounded-2xl overflow-hidden aspect-[4/5] cursor-pointer">
          <div class="absolute inset-0 bg-rose-500/20 mix-blend-overlay group-hover:opacity-0 transition-opacity duration-500 z-10"></div>
          <img :src="img.src" :alt="img.title" class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-700 ease-out" />
          <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500 z-20 flex flex-col justify-end p-6">
            <h3 class="text-xl font-playfair text-white mb-1 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-500">{{ img.title }}</h3>
            <p class="text-rose-200/80 text-sm transform translate-y-4 group-hover:translate-y-0 transition-transform duration-500 delay-75">{{ img.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const gallery = [
  { src: 'https://images.unsplash.com/photo-1562322140-8baeececf3df?auto=format&fit=crop&q=80&w=800', title: 'Balayage Premium', desc: 'Coloración y matiz' },
  { src: 'https://images.unsplash.com/photo-1600948836101-f9ffda59d250?auto=format&fit=crop&q=80&w=800', title: 'Corte Bob Asimétrico', desc: 'Estilismo moderno' },
  { src: 'https://images.unsplash.com/photo-1522337660859-02fbefca4702?auto=format&fit=crop&q=80&w=800', title: 'Maquillaje de Noche', desc: 'Eventos especiales' },
  { src: 'https://images.unsplash.com/photo-1516975080661-46bfa2c22401?auto=format&fit=crop&q=80&w=800', title: 'Tratamiento Keratina', desc: 'Restauración profunda' },
  { src: 'https://images.unsplash.com/photo-1595476108010-b4d1f10d5e43?auto=format&fit=crop&q=80&w=800', title: 'Manicura Rusa', desc: 'Uñas esculpidas' },
  { src: 'https://images.unsplash.com/photo-1580618672591-eb180b1a973f?auto=format&fit=crop&q=80&w=800', title: 'Ondas Surferas', desc: 'Peinado casual' }
];
</script>
