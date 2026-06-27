<template>
  <section class="relative min-h-screen pt-32 pb-20 overflow-hidden bg-salon-secondary flex items-center">
    
    <!-- Decoraciones Orgánicas de Fondo -->
    <div class="absolute top-0 right-0 w-[40vw] h-[40vw] bg-salon-light rounded-bl-full pointer-events-none z-0"></div>
    <div class="absolute bottom-0 left-0 w-[30vw] h-[30vw] bg-salon-primary/10 rounded-tr-full pointer-events-none z-0 blur-3xl"></div>

    <div class="max-w-7xl mx-auto px-6 relative z-10 w-full">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 lg:gap-8 items-center">
        
        <!-- Texto Principal -->
        <div class="flex flex-col justify-center order-2 lg:order-1 text-center lg:text-left reveal-up">
          <div class="flex items-center justify-center lg:justify-start gap-4 mb-6">
            <div class="w-12 h-[1px] bg-salon-primary"></div>
            <span class="text-salon-primary font-sans font-medium tracking-[0.3em] uppercase text-xs">
              Santuario de Belleza
            </span>
          </div>
          
          <h1 class="font-serif text-6xl md:text-7xl lg:text-8xl text-salon-dark mb-6 leading-[1.1] tracking-tight">
            Descubre tu <br/>
            <span class="italic font-light text-salon-primary">esencia natural.</span>
          </h1>
          
          <p class="text-salon-dark/70 font-sans text-lg md:text-xl font-light leading-relaxed mb-10 max-w-lg mx-auto lg:mx-0">
            Un espacio donde el tiempo se detiene y la belleza cobra vida a través de rituales personalizados y maestría artística.
          </p>
          
          <div class="flex flex-col sm:flex-row items-center gap-6 justify-center lg:justify-start">
            <a href="#cita" class="w-full sm:w-auto bg-salon-primary text-salon-secondary px-10 py-4 rounded-full font-sans text-sm font-medium tracking-[0.2em] uppercase hover:bg-salon-dark transition-colors duration-500 shadow-xl shadow-salon-primary/20">
              Reservar Experiencia
            </a>
            <a href="#servicios" class="w-full sm:w-auto text-salon-dark px-6 py-4 font-sans text-sm font-medium tracking-[0.2em] uppercase hover:text-salon-primary transition-colors flex items-center justify-center gap-2 group">
              Descubrir
              <svg class="w-4 h-4 transform group-hover:translate-x-1 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
              </svg>
            </a>
          </div>
        </div>

        <!-- Imagen en Arco -->
        <div class="order-1 lg:order-2 flex justify-center lg:justify-end reveal-left relative">
          <!-- Círculo decorativo giratorio -->
          <div class="absolute top-10 -left-10 w-32 h-32 border border-salon-primary/30 rounded-full animate-[spin_20s_linear_infinite] pointer-events-none hidden md:block"></div>
          
          <!-- Contenedor con forma de arco -->
          <div class="relative w-full max-w-md aspect-[3/4] rounded-t-[200px] overflow-hidden shadow-2xl shadow-salon-dark/10 group">
            <div class="absolute inset-0 bg-salon-dark/10 z-10 group-hover:bg-transparent transition-colors duration-700"></div>
            <img 
              src="https://images.unsplash.com/photo-1522337660859-02fbefca4702?q=80&w=1200&auto=format&fit=crop" 
              alt="Modelo Salón" 
              class="w-full h-full object-cover transform scale-105 group-hover:scale-100 transition-transform duration-[1.5s]"
            />
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
