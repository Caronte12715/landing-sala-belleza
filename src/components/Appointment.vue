<template>
  <section id="cita" class="py-32 bg-salon-light relative overflow-hidden">
    <!-- Círculo decorativo enorme -->
    <div class="absolute -right-1/4 -top-1/4 w-[80vw] h-[80vw] rounded-full bg-salon-secondary z-0 pointer-events-none"></div>

    <div class="max-w-5xl mx-auto px-6 relative z-10">
      <div class="bg-white rounded-[40px] shadow-2xl shadow-salon-dark/5 p-10 md:p-20 reveal-up border border-salon-primary/10">
        
        <div class="text-center mb-16">
          <span class="text-salon-primary font-sans font-medium tracking-[0.3em] uppercase text-xs mb-4 block">
            Tu Momento
          </span>
          <h2 class="font-serif text-5xl md:text-6xl text-salon-dark mb-6">Reserva tu <span class="italic font-light text-salon-primary">Cita</span></h2>
          <div class="w-12 h-[1px] bg-salon-primary mx-auto"></div>
        </div>

        <form class="space-y-12">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
            
            <div class="group relative">
              <input type="text" id="nombre" class="w-full bg-transparent border-b border-salon-dark/20 px-0 py-3 text-salon-dark focus:outline-none focus:border-salon-primary transition-colors font-sans text-lg peer placeholder-transparent" placeholder="Nombre" />
              <label for="nombre" class="absolute left-0 -top-4 text-xs font-sans text-salon-primary tracking-[0.2em] uppercase transition-all peer-placeholder-shown:text-base peer-placeholder-shown:text-salon-dark/50 peer-placeholder-shown:top-3 peer-focus:-top-4 peer-focus:text-xs peer-focus:text-salon-primary">Tu Nombre Completo</label>
            </div>
            
            <div class="group relative">
              <input type="tel" id="telefono" class="w-full bg-transparent border-b border-salon-dark/20 px-0 py-3 text-salon-dark focus:outline-none focus:border-salon-primary transition-colors font-sans text-lg peer placeholder-transparent" placeholder="Teléfono" />
              <label for="telefono" class="absolute left-0 -top-4 text-xs font-sans text-salon-primary tracking-[0.2em] uppercase transition-all peer-placeholder-shown:text-base peer-placeholder-shown:text-salon-dark/50 peer-placeholder-shown:top-3 peer-focus:-top-4 peer-focus:text-xs peer-focus:text-salon-primary">Teléfono / WhatsApp</label>
            </div>
            
            <div class="group relative">
              <label class="block text-xs font-sans text-salon-primary tracking-[0.2em] uppercase mb-2">Servicio Deseado</label>
              <select class="w-full bg-transparent border-b border-salon-dark/20 px-0 py-3 text-salon-dark focus:outline-none focus:border-salon-primary transition-colors font-sans text-lg appearance-none cursor-pointer">
                <option>Corte y Estilo</option>
                <option>Coloración Premium (Balayage)</option>
                <option>Tratamiento Capilar Profundo</option>
                <option>Maquillaje Social / Novias</option>
                <option>Asesoría de Imagen</option>
              </select>
            </div>
            
            <div class="group relative">
              <label class="block text-xs font-sans text-salon-primary tracking-[0.2em] uppercase mb-2">Fecha Preferida</label>
              <input type="date" class="w-full bg-transparent border-b border-salon-dark/20 px-0 py-3 text-salon-dark focus:outline-none focus:border-salon-primary transition-colors font-sans text-lg cursor-pointer" />
            </div>
            
          </div>
          
          <div class="pt-8 text-center">
            <button type="button" class="bg-salon-dark text-salon-secondary px-12 py-5 rounded-full font-sans text-sm font-medium tracking-[0.2em] uppercase hover:bg-salon-primary transition-colors duration-500 shadow-xl shadow-salon-dark/10 w-full md:w-auto">
              Confirmar Reservación
            </button>
          </div>
        </form>

      </div>
    </div>
  </section>
</template>
