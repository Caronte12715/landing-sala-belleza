<template>
  <footer class="bg-salon-dark text-salon-secondary pt-32 pb-12 relative overflow-hidden">
    <div class="max-w-7xl mx-auto px-6 relative z-10">
      
      <div class="grid grid-cols-1 md:grid-cols-12 gap-16 mb-24">
        
        <div class="md:col-span-5 reveal-up">
          <a href="#" class="flex flex-col items-start mb-8">
            <span class="font-serif text-4xl font-light tracking-widest text-salon-secondary leading-none mb-2">A U R E A</span>
            <span class="font-sans text-[0.6rem] tracking-[0.4em] text-salon-primary uppercase">Slow Beauty</span>
          </a>
          <p class="text-salon-secondary/60 font-sans font-light text-sm max-w-sm leading-relaxed">
            Redefiniendo los estándares de belleza a través de una experiencia sensorial íntima, productos orgánicos y diseño atemporal.
          </p>
        </div>

        <div class="md:col-span-3 reveal-up delay-100">
          <h4 class="font-sans text-salon-primary text-xs tracking-[0.3em] uppercase mb-6 font-medium">Ubicación</h4>
          <p class="text-salon-secondary/80 font-sans font-light text-sm leading-relaxed">
            Avenida de la Luz 450<br/>
            Distrito Financiero<br/>
            Ciudad Metrópolis, 10293
          </p>
        </div>

        <div class="md:col-span-4 reveal-up delay-200">
          <h4 class="font-sans text-salon-primary text-xs tracking-[0.3em] uppercase mb-6 font-medium">Contacto & Horarios</h4>
          <p class="text-salon-secondary/80 font-sans font-light text-sm leading-relaxed mb-4">
            contacto@aurea-salon.com<br/>
            +1 234 567 8900
          </p>
          <p class="text-salon-secondary/60 font-sans font-light text-sm">
            Martes - Sábado: 10:00 - 19:00<br/>
            Domingo y Lunes: Cerrado
          </p>
        </div>

      </div>

      <div class="border-t border-salon-secondary/10 pt-8 flex flex-col md:flex-row justify-between items-center gap-6 reveal-up delay-300">
        <p class="text-salon-secondary/40 font-sans text-xs font-light">
          &copy; {{ new Date().getFullYear() }} AUREA Slow Beauty. Todos los derechos reservados.
        </p>
        <div class="flex items-center gap-6">
          <a href="#" class="text-salon-secondary/40 hover:text-salon-primary transition-colors font-sans text-xs tracking-widest uppercase">Instagram</a>
          <a href="#" class="text-salon-secondary/40 hover:text-salon-primary transition-colors font-sans text-xs tracking-widest uppercase">Pinterest</a>
        </div>
      </div>
      
    </div>
  </footer>
</template>
