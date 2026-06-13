<template>
  <section id="reserva" class="py-24 relative overflow-hidden bg-[#1E0B16]">
    <div class="absolute inset-0 bg-gradient-to-t from-[#0A000A] to-transparent opacity-80 z-0"></div>
    <div class="max-w-4xl mx-auto px-6 relative z-10">
      <div class="bg-white/5 backdrop-blur-2xl border border-white/10 rounded-3xl p-8 md:p-12 shadow-[0_0_50px_rgba(225,29,72,0.1)]">
        <div class="text-center mb-10">
          <h2 class="text-3xl md:text-5xl font-playfair text-white mb-4">Agenda tu <span class="text-rose-400">Momento</span></h2>
          <p class="text-rose-100/70">Déjanos tus datos y nos pondremos en contacto para confirmar tu cita.</p>
        </div>

        <form class="space-y-6">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="space-y-2">
              <label class="text-sm font-medium text-gray-300">Nombre Completo</label>
              <input type="text" class="w-full bg-black/40 border border-white/10 rounded-xl px-4 py-3 text-white placeholder-gray-500 focus:outline-none focus:border-rose-500 focus:ring-1 focus:ring-rose-500 transition-all" placeholder="Tu nombre" />
            </div>
            <div class="space-y-2">
              <label class="text-sm font-medium text-gray-300">Teléfono</label>
              <input type="tel" class="w-full bg-black/40 border border-white/10 rounded-xl px-4 py-3 text-white placeholder-gray-500 focus:outline-none focus:border-rose-500 focus:ring-1 focus:ring-rose-500 transition-all" placeholder="Tu WhatsApp" />
            </div>
          </div>
          
          <div class="space-y-2">
            <label class="text-sm font-medium text-gray-300">Servicio de Interés</label>
            <select class="w-full bg-black/40 border border-white/10 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-rose-500 transition-all appearance-none">
              <option value="" class="bg-[#1E0B16]">Selecciona un servicio...</option>
              <option value="corte" class="bg-[#1E0B16]">Corte y Estilismo</option>
              <option value="color" class="bg-[#1E0B16]">Colorimetría y Balayage</option>
              <option value="tratamiento" class="bg-[#1E0B16]">Tratamientos Capilares</option>
              <option value="maquillaje" class="bg-[#1E0B16]">Maquillaje Profesional</option>
            </select>
          </div>

          <div class="space-y-2">
            <label class="text-sm font-medium text-gray-300">Fecha Preferida</label>
            <input type="date" class="w-full bg-black/40 border border-white/10 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-rose-500 transition-all" />
          </div>

          <button type="button" class="w-full py-4 bg-gradient-to-r from-rose-500 to-pink-500 text-white font-bold rounded-xl shadow-[0_0_20px_rgba(225,29,72,0.4)] hover:shadow-[0_0_30px_rgba(225,29,72,0.6)] hover:-translate-y-1 transition-all duration-300">
            Solicitar Cita
          </button>
        </form>
      </div>
    </div>
  </section>
</template>
