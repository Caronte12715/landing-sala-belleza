<script setup>
const services = [
  {
    title: 'Corte y Estilismo',
    description: 'Nuestros estilistas crean looks personalizados que realzan tus mejores rasgos, utilizando las últimas tendencias y técnicas.',
    icon: '✂️',
    price: 'Desde $45'
  },
  {
    title: 'Coloración Premium',
    description: 'Balayage, babylights o cambios completos. Usamos productos de alta gama que protegen la salud de tu cabello.',
    icon: '🎨',
    price: 'Desde $85'
  },
  {
    title: 'Manicura Spa',
    description: 'Cuidado completo para tus manos con esmaltes duraderos y tratamientos hidratantes profundos.',
    icon: '💅',
    price: 'Desde $30'
  },
  {
    title: 'Tratamientos Faciales',
    description: 'Revitaliza tu piel con limpiezas profundas, hidratación y tratamientos antienvejecimiento personalizados.',
    icon: '✨',
    price: 'Desde $65'
  }
];
</script>

<template>
  <section id="servicios" class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-6">
      
      <div class="text-center mb-16 max-w-2xl mx-auto">
        <span class="text-salon-primary font-semibold tracking-widest uppercase text-sm mb-4 block">
          Nuestro Menú
        </span>
        <h2 class="text-4xl md:text-5xl text-salon-dark mb-6">Servicios Destacados</h2>
        <div class="w-24 h-1 bg-salon-primary mx-auto mb-6"></div>
        <p class="text-gray-500 text-lg font-light">
          Cada servicio está diseñado para ofrecerte una experiencia de relajación total y resultados excepcionales.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div 
          v-for="(service, index) in services" 
          :key="index"
          class="bg-salon-light p-10 group hover:bg-salon-dark transition-colors duration-500 flex flex-col items-center text-center"
        >
          <div class="text-4xl mb-6 grayscale opacity-80 group-hover:grayscale-0 group-hover:opacity-100 transition-all duration-500 transform group-hover:scale-110">
            {{ service.icon }}
          </div>
          <h3 class="text-2xl mb-4 text-salon-dark group-hover:text-white transition-colors duration-500">
            {{ service.title }}
          </h3>
          <p class="text-gray-500 mb-8 font-light text-sm leading-relaxed group-hover:text-gray-400 transition-colors duration-500 flex-grow">
            {{ service.description }}
          </p>
          <div class="text-salon-primary font-bold tracking-wider">
            {{ service.price }}
          </div>
        </div>
      </div>

    </div>
  </section>
</template>
