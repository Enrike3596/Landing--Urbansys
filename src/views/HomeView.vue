<script setup>
import { ref } from 'vue'

const isDarkMode = ref(false)

const toggleDarkMode = () => {
  isDarkMode.value = !isDarkMode.value
  if (isDarkMode.value) {
    document.documentElement.classList.add('dark')
  } else {
    document.documentElement.classList.remove('dark')
  }
}
</script>

<template>
  <!-- Top Navigation -->
  <header class="fixed top-0 w-full z-50 bg-white/80 dark:bg-slate-950/90 backdrop-blur-xl shadow-sm dark:shadow-lg dark:shadow-blue-500/10 bg-opacity-90">
    <nav class="flex justify-between items-center px-6 py-2 max-w-7xl mx-auto">
      <div class="flex items-center gap-3">
        <img alt="Urbansys Logo" src="@/assets/Img/LogoUrbansys-Photoroom.png" class="w-40 h-20 -my-2">
      </div>
      <div class="hidden md:flex items-center space-x-8 font-bold tracking-tight">
        <a href="#mission" class="text-slate-600 dark:text-slate-300 font-medium hover:text-blue-700 dark:hover:text-blue-300 transition-colors duration-300">Misión</a>
        <a href="#vision" class="text-slate-600 dark:text-slate-300 font-medium hover:text-blue-700 dark:hover:text-blue-300 transition-colors duration-300">Visión</a>
        <a href="#services" class="text-slate-600 dark:text-slate-300 font-medium hover:text-blue-700 dark:hover:text-blue-300 transition-colors duration-300">Servicios</a>
        <a href="#contact" class="text-slate-600 dark:text-slate-300 font-medium hover:text-blue-700 dark:hover:text-blue-300 transition-colors duration-300">Contacto</a>
      </div>
      <div class="flex items-center gap-4">
        <button @click="toggleDarkMode" class="relative group p-2.5 rounded-full bg-gradient-to-br from-slate-50 to-slate-100 dark:from-slate-700 dark:to-slate-800 hover:from-blue-50 hover:to-blue-100 dark:hover:from-blue-900/40 dark:hover:to-blue-800/40 transition-all duration-300 text-slate-600 dark:text-slate-300 active:scale-90 shadow-sm hover:shadow-md" aria-label="Cambiar tema claro/oscuro">
          <div class="absolute inset-0 rounded-full bg-gradient-to-r from-blue-400/0 to-purple-400/0 dark:from-blue-500/10 dark:to-purple-500/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          <div class="relative z-10 flex items-center">
            <div class="relative w-14 h-7 flex items-center px-1 rounded-full bg-slate-200 dark:bg-slate-700 transition-colors duration-300">
              <div class="absolute w-6 h-6 bg-white rounded-full shadow transform transition-transform duration-300" :class="isDarkMode ? 'translate-x-7' : 'translate-x-0'"></div>
              <span class="material-symbols-outlined text-[18px] text-amber-400 z-10">light_mode</span>
              <span class="material-symbols-outlined text-[18px] text-blue-300 ml-auto z-10">dark_mode</span>
            </div>
          </div>
        </button>
      </div>
    </nav>
  </header>

  <main class="pt-20 scroll-smooth">
    <!-- Hero Section -->
    <section class="relative min-h-screen flex items-start justify-center overflow-hidden pt-20">
      <div class="absolute inset-0 z-0">
        <div class="absolute inset-0 bg-gradient-to-br from-blue-100 via-blue-50 to-slate-50 dark:from-slate-900 dark:via-slate-900 dark:to-slate-950"></div>
        <div class="absolute inset-0 bg-gradient-to-b from-transparent via-transparent to-white/30 dark:to-black/40"></div>
        <img alt="Detalles arquitectónicos de rascacielos" class="w-full h-full object-cover opacity-10 dark:opacity-5" src="https://lh3.googleusercontent.com/aida-public/AB6AXuBXyKadXP2j99Wh98Pu4uZ5X0UHCGDLPAzUJYvzGkghhkcA_dUuSvRxgTBFPXCRSvC2DcSZnfgaZ1f2kOCM6xmyetOOvIfq26MZYn3ZBRyeq3toPBB8Atk34K12XyaiH8lmiOF5d2REVe4g0WjpO2MOdCtrGeRcnBWFfpMLiMW8A99oSUoGWI0zTEdLkHOQtQzaizBnY6BWBwKX054wJYKDZ--Hb61mU_L5dK86LlNuF3ClWDnDjSkIioOsYA0IlxzqawRoNTUx62M"/>
      </div>

      <!-- Decorative gradient orbs -->
      <div class="absolute top-20 right-10 w-72 h-72 bg-gradient-to-br from-blue-400/20 to-purple-400/20 dark:from-blue-500/10 dark:to-purple-500/10 rounded-full blur-3xl"></div>
      <div class="absolute bottom-20 left-10 w-72 h-72 bg-gradient-to-br from-cyan-400/20 to-green-400/20 dark:from-cyan-500/10 dark:to-green-500/10 rounded-full blur-3xl"></div>

      <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 lg:grid-cols-2 gap-8 relative z-10 items-start lg:items-start">
        <!-- Hero Content -->
        <div class="flex flex-col justify-center space-y-8">
          <div class="space-y-4">
            <div class="inline-block">
              <span class="bg-gradient-to-r from-blue-600 to-cyan-600 dark:from-blue-400 dark:to-cyan-400 text-white px-4 py-2 rounded-full text-sm font-bold uppercase tracking-widest">Revolución Digital</span>
            </div>
            <h1 class="font-headline font-extrabold text-5xl md:text-6xl lg:text-7xl text-primary dark:text-white leading-tight">
              La Gestión Residencial Inteligente.
            </h1>
          </div>

          <p class="text-lg md:text-xl text-slate-700 dark:text-slate-200 max-w-xl leading-relaxed">
            Urbansys es la plataforma todo-en-uno que transforma la administración de comunidades residenciales. Centraliza información, automatiza procesos, mejora la comunicación entre residentes y administradores, y proporciona reportes inteligentes para tomar decisiones basadas en datos reales. Desde censos digitales hasta reservas de amenities y parqueo, todo en una interfaz intuitiva y segura.
          </p>

          <div class="flex flex-col sm:flex-row gap-4 pt-4">
            <button class="bg-gradient-to-br from-primary to-primary-container text-white px-8 py-4 rounded-2xl font-bold text-lg shadow-lg hover:shadow-2xl hover:shadow-primary/50 hover:-translate-y-1 hover:scale-105 transition-all active:scale-95">
              Comenzar Ahora
            </button>
            <button class="bg-white/90 dark:bg-slate-700/90 text-primary dark:text-slate-200 px-8 py-4 rounded-2xl font-bold text-lg border-2 border-primary dark:border-slate-600 hover:bg-white dark:hover:bg-slate-700 hover:-translate-y-1 hover:scale-105 transition-all shadow-md hover:shadow-lg backdrop-blur-sm">
              Ver Demo
            </button>
          </div>

          <!-- Stats -->
          <div class="grid grid-cols-3 gap-6 pt-8 border-t border-slate-200 dark:border-slate-700">
            <div>
              <div class="text-3xl font-black text-primary dark:text-blue-400">1000+</div>
              <p class="text-sm text-on-surface-variant dark:text-slate-400 mt-1">Comunidades</p>
            </div>
            <div>
              <div class="text-3xl font-black text-primary dark:text-blue-400">50K+</div>
              <p class="text-sm text-on-surface-variant dark:text-slate-400 mt-1">Usuarios Activos</p>
            </div>
            <div>
              <div class="text-3xl font-black text-primary dark:text-blue-400">98%</div>
              <p class="text-sm text-on-surface-variant dark:text-slate-400 mt-1">Satisfacción</p>
            </div>
          </div>
        </div>

        <!-- Live Panel - Right Side -->
        <div class="relative hidden lg:block">
          <div class="absolute -inset-6 bg-gradient-to-br from-blue-500/20 to-cyan-500/20 dark:from-blue-900/30 dark:to-cyan-900/30 rounded-3xl blur-3xl"></div>
          <div class="relative bg-white/95 dark:bg-slate-800/95 backdrop-blur-xl p-6 rounded-3xl shadow-2xl border border-slate-200/50 dark:border-slate-700/50">
            <!-- Header -->
            <div class="flex items-center justify-between mb-6 pb-4 border-b border-slate-200 dark:border-slate-700">
              <div>
                <h3 class="font-headline font-bold text-2xl text-primary dark:text-slate-100">Panel en Vivo</h3>
                <p class="text-xs text-on-surface-variant dark:text-slate-500 mt-1.5 font-medium">En tiempo real</p>
              </div>
              <div class="w-12 h-12 rounded-full bg-gradient-to-br from-green-500 to-green-600 flex items-center justify-center text-white shadow-lg animate-pulse">
                <span class="material-symbols-outlined text-xl">check_circle</span>
              </div>
            </div>

            <!-- Main Stat -->
            <div class="mb-4 p-5 bg-gradient-to-br from-blue-50 to-blue-100 dark:from-blue-950/40 dark:to-blue-900/40 rounded-2xl border border-blue-200 dark:border-blue-800/50">
              <div class="text-xs font-bold uppercase tracking-widest text-blue-700 dark:text-blue-300 mb-2">Total de Residentes</div>
              <div class="flex items-baseline justify-between">
              <div class="text-4xl font-black text-blue-600 dark:text-blue-100">1,248</div>
                <div class="text-sm font-bold text-green-600 dark:text-green-400 bg-green-100 dark:bg-green-950/50 px-3 py-1 rounded-full">↑ +12 mes</div>
              </div>
            </div>

            <!-- Two Columns Stats -->
            <div class="grid grid-cols-2 gap-3 mb-4">
              <div class="p-4 bg-gradient-to-br from-green-50 to-green-100 dark:from-green-950/40 dark:to-green-900/40 rounded-xl border border-green-200 dark:border-green-800/50">
                <div class="text-[11px] font-bold uppercase tracking-widest text-green-700 dark:text-green-300 mb-2">Ocupación</div>
                <div class="text-3xl font-black text-green-600 dark:text-green-100">98%</div>
                <div class="text-xs text-green-600 dark:text-green-400 mt-1 font-semibold">Óptimo</div>
              </div>
              <div class="p-4 bg-gradient-to-br from-amber-50 to-amber-100 dark:from-amber-950/40 dark:to-amber-900/40 rounded-xl border border-amber-200 dark:border-amber-800/50">
                <div class="text-[11px] font-bold uppercase tracking-widest text-amber-700 dark:text-amber-300 mb-2">Solicitudes</div>
                <div class="text-3xl font-black text-amber-600 dark:text-amber-100">24</div>
                <div class="text-xs text-amber-600 dark:text-amber-400 mt-1 font-semibold">Activas</div>
              </div>
            </div>

            <!-- Progress Bar -->
            <div class="pt-4 border-t border-slate-200 dark:border-slate-700">
              <div class="flex items-center justify-between mb-2">
                <span class="text-xs font-bold text-on-surface-variant dark:text-slate-400 uppercase tracking-wide">Eficiencia del Sistema</span>
                <span class="text-sm font-bold text-primary dark:text-cyan-400">94%</span>
              </div>
              <div class="w-full h-2.5 bg-slate-200 dark:bg-slate-700 rounded-full overflow-hidden">
                <div class="h-full bg-gradient-to-r from-green-500 via-cyan-500 to-blue-500 rounded-full" style="width: 94%"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Problem / Solution Section -->
    <section class="py-24 bg-surface-container-low dark:bg-slate-900">
      <div class="max-w-7xl mx-auto px-6">
        <div class="mb-16 text-center max-w-2xl mx-auto">
          <h2 class="font-headline font-bold text-4xl text-primary dark:text-primary-fixed mb-4 tracking-tight">Solucionando la Fricción del Residente</h2>
          <p class="text-on-surface-variant dark:text-slate-400">La gestión tradicional está obsoleta. La reconstruimos desde cero para la era digital.</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <!-- Problem Card -->
          <div class="md:col-span-1 bg-surface-container-lowest dark:bg-slate-800 p-8 rounded-2xl flex flex-col justify-between group hover:shadow-xl hover:-translate-y-2 transition-all border border-transparent hover:border-outline-variant/10">
            <div>
              <span class="material-symbols-outlined text-error text-4xl mb-6 group-hover:scale-110 transition-transform" data-weight="fill">dangerous</span>
              <h3 class="font-headline font-bold text-2xl text-on-surface dark:text-white mb-4">La Realidad Desordenada</h3>
              <p class="text-on-surface-variant dark:text-slate-400 leading-relaxed">Registros en papel, correos perdidos y grupos caóticos de WhatsApp crean un entorno de desconfianza e ineficiencia.</p>
            </div>
            <ul class="mt-8 space-y-3">
              <li class="flex items-center gap-3 text-sm text-on-surface-variant dark:text-slate-400">
                <span class="material-symbols-outlined text-error text-sm">close</span> Registros dispersos
              </li>
              <li class="flex items-center gap-3 text-sm text-on-surface-variant dark:text-slate-400">
                <span class="material-symbols-outlined text-error text-sm">close</span> Brechas de comunicación
              </li>
            </ul>
          </div>

          <!-- Solution Card -->
          <div class="md:col-span-2 bg-primary dark:bg-blue-950 p-12 rounded-2xl relative overflow-hidden flex flex-col justify-center text-on-primary group hover:shadow-2xl transition-all">
            <div class="absolute top-0 right-0 w-64 h-64 bg-primary-container/30 rounded-full -mr-20 -mt-20 blur-3xl group-hover:scale-110 transition-transform duration-700"></div>
            <div class="relative z-10">
              <h3 class="font-headline font-bold text-4xl mb-6">Arquitectura Tonal Unificada</h3>
              <p class="text-lg opacity-80 max-w-lg mb-10 leading-relaxed">
                System Urbansys reemplaza el ruido por claridad. Una única fuente de verdad para toda su comunidad, envuelta en una interfaz premium que los residentes realmente disfrutan usar.
              </p>
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-8">
                <div class="flex items-start gap-4 hover:translate-x-2 transition-transform">
                  <div class="bg-white/10 p-3 rounded-lg"><span class="material-symbols-outlined text-tertiary-fixed">verified</span></div>
                  <div>
                    <div class="font-bold">Claridad en tiempo real</div>
                    <div class="text-sm opacity-60">Actualizaciones instantáneas para todos.</div>
                  </div>
                </div>
                <div class="flex items-start gap-4 hover:translate-x-2 transition-transform">
                  <div class="bg-white/10 p-3 rounded-lg"><span class="material-symbols-outlined text-tertiary-fixed">security</span></div>
                  <div>
                    <div class="font-bold">Confianza encriptada</div>
                    <div class="text-sm opacity-60">Sus datos, asegurados para siempre.</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Mission & Vision Section -->
    <section id="mission" class="py-32 overflow-hidden bg-surface-container-lowest dark:bg-slate-950">
      <div class="max-w-7xl mx-auto px-6">
        <div class="flex flex-col lg:flex-row gap-20 items-center">
          <div class="lg:w-1/2 relative group">
            <div class="absolute -inset-10 bg-surface-container/50 dark:bg-blue-900/20 rounded-full blur-3xl group-hover:scale-110 transition-transform duration-1000"></div>
            <img alt="Lobby de oficina minimalista" class="rounded-[2.5rem] shadow-2xl relative z-10 w-full aspect-square object-cover transition-transform duration-500 group-hover:scale-[1.02]" src="https://lh3.googleusercontent.com/aida-public/AB6AXuD_YiBIEbh_D8Pg83mLkcO623T0L_FNzGh92MzhFX88gl4zcPeOedZoS6TkOU3X6VZWPxDXQs06dMKZ4TkpsJ5VedpOeDVYHibnxiBvdA8_mBonroaYBC_iVqtnCXtLxzDB8MFQVBRe-DWG3sQK8BJGBwKfmvGtYNqJsJhWFQrLMBrgGhS1pEKv12RTmVVKXMP3U395_22A1z1CgUw68I-d1QtwqJrT71NgA2SzT9xeDWXTFyWGjOSfLxxSu9BroTi3SicaSi8qW3Y"/>
          </div>
          <div class="lg:w-1/2">
            <div class="space-y-12">
              <div>
                <span class="text-tertiary dark:text-tertiary-fixed font-black tracking-widest text-xs uppercase mb-4 block">Nuestra Identidad</span>
                <h2 class="font-headline font-extrabold text-4xl text-primary dark:text-primary-fixed mb-6">Misión</h2>
                <p class="text-xl text-on-surface-variant dark:text-slate-400 leading-relaxed font-light">
                  Transformar la gestión residencial de una carga logística a una experiencia de servicio fluida, fomentando la confianza a través de una transparencia radical y un diseño digital superior.
                </p>
              </div>
              <div class="h-px bg-surface-container dark:bg-slate-800 max-w-sm"></div>
              <div id="vision">
                <h2 class="font-headline font-extrabold text-4xl text-primary dark:text-primary-fixed mb-6">Visión</h2>
                <p class="text-xl text-on-surface-variant dark:text-slate-400 leading-relaxed font-light">
                  Establecer el estándar global para la vida residencial de alta gama, donde la tecnología actúa como un conserje invisible y sofisticado para cada urbanita moderno.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- About Us / Lo que Ofrecemos Section -->
    <section class="py-24 bg-gradient-to-b from-surface-container-lowest to-surface-container-low dark:from-slate-950 dark:to-slate-900">
      <div class="max-w-7xl mx-auto px-6">
        <div class="mb-20 text-center max-w-3xl mx-auto">
          <span class="text-tertiary dark:text-tertiary-fixed font-black tracking-widest text-xs uppercase mb-4 block">Sobre Urbansys</span>
          <h2 class="font-headline font-bold text-5xl text-primary dark:text-white mb-6">Lo Que Ofrecemos</h2>
          <p class="text-lg text-on-surface-variant dark:text-slate-300">Urbansys es una plataforma integral de gestión residencial diseñada para modernizar la experiencia de los residentes y simplificar la administración de comunidades.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- Feature 1 -->
          <div class="group bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all border border-slate-200 dark:border-slate-700">
            <div class="w-20 h-20 bg-gradient-to-br from-blue-500 to-blue-600 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-blue-500/50 transition-all transform">
              <span class="material-symbols-outlined text-white text-5xl">dashboard</span>
            </div>
            <h3 class="font-headline font-bold text-xl text-on-surface dark:text-white mb-3">Panel de Control Centralizado</h3>
            <p class="text-on-surface-variant dark:text-slate-400">Acceso único y simplificado a toda la información de tu comunidad en tiempo real.</p>
          </div>

          <!-- Feature 2 -->
          <div class="group bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all border border-slate-200 dark:border-slate-700">
            <div class="w-20 h-20 bg-gradient-to-br from-green-500 to-green-600 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-green-500/50 transition-all transform">
              <span class="material-symbols-outlined text-white" style="font-size: 56px; font-weight: 400;">verified</span>
            </div>
            <h3 class="font-headline font-bold text-xl text-on-surface dark:text-white mb-3">Seguridad de Nivel Empresarial</h3>
            <p class="text-on-surface-variant dark:text-slate-400">Encriptación end-to-end y cumplimiento con estándares internacionales de protección de datos.</p>
          </div>

          <!-- Feature 3 -->
          <div class="group bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all border border-slate-200 dark:border-slate-700">
            <div class="w-20 h-20 bg-gradient-to-br from-purple-500 to-purple-600 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-purple-500/50 transition-all transform">
              <span class="material-symbols-outlined text-white text-5xl">integration_instructions</span>
            </div>
            <h3 class="font-headline font-bold text-xl text-on-surface dark:text-white mb-3">Integración Total</h3>
            <p class="text-on-surface-variant dark:text-slate-400">Conecta con sistemas existentes y herramientas que ya utilizas en tu comunidad.</p>
          </div>

          <!-- Feature 4 -->
          <div class="group bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all border border-slate-200 dark:border-slate-700">
            <div class="w-20 h-20 bg-gradient-to-br from-amber-500 to-amber-600 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-amber-500/50 transition-all transform">
              <span class="material-symbols-outlined text-white text-5xl">people_alt</span>
            </div>
            <h3 class="font-headline font-bold text-xl text-on-surface dark:text-white mb-3">Comunicación Eficiente</h3>
            <p class="text-on-surface-variant dark:text-slate-400">Canales de comunicación directa y notificaciones automáticas para residentes y administradores.</p>
          </div>

          <!-- Feature 5 -->
          <div class="group bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all border border-slate-200 dark:border-slate-700">
            <div class="w-20 h-20 bg-gradient-to-br from-red-500 to-red-600 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-red-500/50 transition-all transform">
              <span class="material-symbols-outlined text-white text-5xl">analytics</span>
            </div>
            <h3 class="font-headline font-bold text-xl text-on-surface dark:text-white mb-3">Reportes e Informes</h3>
            <p class="text-on-surface-variant dark:text-slate-400">Análisis detallados y reportes personalizados para tomar decisiones informadas.</p>
          </div>

          <!-- Feature 6 -->
          <div class="group bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all border border-slate-200 dark:border-slate-700">
            <div class="w-20 h-20 bg-gradient-to-br from-cyan-500 to-cyan-600 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-cyan-500/50 transition-all transform">
              <span class="material-symbols-outlined text-white" style="font-size: 56px; font-weight: 400;">support_agent</span>
            </div>
            <h3 class="font-headline font-bold text-xl text-on-surface dark:text-white mb-3">Soporte 24/7</h3>
            <p class="text-on-surface-variant dark:text-slate-400">Equipo de soporte técnico disponible todos los días para resolver tus dudas.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Benefits Section -->
    <section class="py-24 bg-white dark:bg-slate-950 overflow-hidden">
      <div class="max-w-7xl mx-auto px-6">
        <div class="mb-20 text-center max-w-3xl mx-auto">
          <span class="text-secondary dark:text-secondary-fixed font-black tracking-widest text-xs uppercase mb-4 block">Ventajas Competitivas</span>
          <h2 class="font-headline font-bold text-5xl text-primary dark:text-white mb-6">Beneficios de Elegir Urbansys</h2>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <!-- Benefits List -->
          <div class="space-y-6">
            <div class="flex gap-4 group">
              <div class="flex-shrink-0 w-16 h-16 rounded-2xl bg-gradient-to-br from-green-500 to-green-600 flex items-center justify-center group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-green-500/50 transition-all transform">
                <span class="material-symbols-outlined text-white text-4xl">check_circle</span>
              </div>
              <div class="group-hover:translate-x-2 transition-transform pt-1">
                <h4 class="font-bold text-lg text-on-surface dark:text-white mb-1">Reducción de Costos Operativos</h4>
                <p class="text-on-surface-variant dark:text-slate-400">Automatiza procesos y reduce gastos administrativos hasta 40%.</p>
              </div>
            </div>

            <div class="flex gap-4 group">
              <div class="flex-shrink-0 w-16 h-16 rounded-2xl bg-gradient-to-br from-blue-500 to-blue-600 flex items-center justify-center group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-blue-500/50 transition-all transform">
                <span class="material-symbols-outlined text-white text-4xl">trending_up</span>
              </div>
              <div class="group-hover:translate-x-2 transition-transform pt-1">
                <h4 class="font-bold text-lg text-on-surface dark:text-white mb-1">Mejor Experiencia de Residentes</h4>
                <p class="text-on-surface-variant dark:text-slate-400">Aumenta la satisfacción y retención con una plataforma intuitiva y moderna.</p>
              </div>
            </div>

            <div class="flex gap-4 group">
              <div class="flex-shrink-0 w-16 h-16 rounded-2xl bg-gradient-to-br from-purple-500 to-purple-600 flex items-center justify-center group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-purple-500/50 transition-all transform">
                <span class="material-symbols-outlined text-white text-4xl">lock</span>
              </div>
              <div class="group-hover:translate-x-2 transition-transform pt-1">
                <h4 class="font-bold text-lg text-on-surface dark:text-white mb-1">Cumplimiento Normativo</h4>
                <p class="text-on-surface-variant dark:text-slate-400">Asegurada conformidad con regulaciones locales e internacionales.</p>
              </div>
            </div>

            <div class="flex gap-4 group">
              <div class="flex-shrink-0 w-16 h-16 rounded-2xl bg-gradient-to-br from-amber-500 to-amber-600 flex items-center justify-center group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-amber-500/50 transition-all transform">
                <span class="material-symbols-outlined text-white text-4xl">schedule</span>
              </div>
              <div class="group-hover:translate-x-2 transition-transform pt-1">
                <h4 class="font-bold text-lg text-on-surface dark:text-white mb-1">Implementación Rápida</h4>
                <p class="text-on-surface-variant dark:text-slate-400">Operacional en 15 días sin disrupciones a tu operación actual.</p>
              </div>
            </div>

            <div class="flex gap-4 group">
              <div class="flex-shrink-0 w-16 h-16 rounded-2xl bg-gradient-to-br from-cyan-500 to-cyan-600 flex items-center justify-center group-hover:scale-110 group-hover:shadow-lg group-hover:shadow-cyan-500/50 transition-all transform">
                <span class="material-symbols-outlined text-white text-4xl">devices</span>
              </div>
              <div class="group-hover:translate-x-2 transition-transform pt-1">
                <h4 class="font-bold text-lg text-on-surface dark:text-white mb-1">Acceso Multiplataforma</h4>
                <p class="text-on-surface-variant dark:text-slate-400">Disponible en web, iOS y Android para acceso desde cualquier lugar.</p>
              </div>
            </div>
          </div>

          <!-- Benefits Image/Graphic -->
          <div class="relative">
            <div class="absolute -inset-4 bg-gradient-to-br from-primary/10 to-secondary/10 dark:from-blue-900/20 dark:to-cyan-900/20 rounded-3xl blur-2xl"></div>
            <div class="relative bg-gradient-to-br from-slate-50 to-slate-100 dark:from-slate-800 dark:to-slate-900 p-12 rounded-3xl border border-slate-200 dark:border-slate-700">
              <div class="space-y-6">
                <div class="flex items-center justify-between">
                  <div>
                    <div class="text-4xl font-black text-primary dark:text-blue-400">40%</div>
                    <div class="text-sm text-on-surface-variant dark:text-slate-400 font-medium">Reducción de costos</div>
                  </div>
                  <span class="material-symbols-outlined text-6xl text-green-500/30">trending_up</span>
                </div>
                <div class="h-px bg-slate-200 dark:bg-slate-700"></div>
                <div class="flex items-center justify-between">
                  <div>
                    <div class="text-4xl font-black text-secondary dark:text-cyan-400">98%</div>
                    <div class="text-sm text-on-surface-variant dark:text-slate-400 font-medium">Satisfacción de usuarios</div>
                  </div>
                  <span class="material-symbols-outlined text-6xl text-blue-500/30">star</span>
                </div>
                <div class="h-px bg-slate-200 dark:bg-slate-700"></div>
                <div class="flex items-center justify-between">
                  <div>
                    <div class="text-4xl font-black text-tertiary dark:text-green-400">1000+</div>
                    <div class="text-sm text-on-surface-variant dark:text-slate-400 font-medium">Comunidades activas</div>
                  </div>
                  <span class="material-symbols-outlined text-6xl text-cyan-500/30">home</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-24 bg-gradient-to-b from-surface-container-low to-surface-container-lowest dark:from-slate-900 dark:to-slate-950">
      <div class="max-w-7xl mx-auto px-6">
        <div class="mb-20 text-center max-w-3xl mx-auto">
          <span class="text-tertiary-fixed dark:text-tertiary font-black tracking-widest text-xs uppercase mb-4 block">Lo Que Dicen Nuestros Clientes</span>
          <h2 class="font-headline font-bold text-5xl text-primary dark:text-white mb-6">Testimonios de Satisfacción</h2>
          <p class="text-lg text-on-surface-variant dark:text-slate-300">Escucha a administradores y residentes que ya transformaron sus comunidades con Urbansys.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- Testimonial 1 -->
          <div class="bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all border border-slate-200 dark:border-slate-700">
            <div class="flex items-center gap-1 mb-4">
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
            </div>
            <p class="text-on-surface dark:text-slate-300 mb-6 leading-relaxed italic">"Urbansys transformó completamente la administración de nuestro conjunto. Desde el primer mes vimos una reducción significativa en costos y los residentes están mucho más satisfechos."</p>
            <div class="flex items-center gap-3 pt-4 border-t border-slate-200 dark:border-slate-700">
              <div class="w-12 h-12 rounded-full bg-gradient-to-br from-blue-500 to-blue-600 flex items-center justify-center text-white font-bold text-lg">JC</div>
              <div>
                <div class="font-bold text-on-surface dark:text-white">Juan Carlos López</div>
                <div class="text-xs text-on-surface-variant dark:text-slate-500">Administrador, Conjunto Empresarial</div>
              </div>
            </div>
          </div>

          <!-- Testimonial 2 -->
          <div class="bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all border border-slate-200 dark:border-slate-700">
            <div class="flex items-center gap-1 mb-4">
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
            </div>
            <p class="text-on-surface dark:text-slate-300 mb-6 leading-relaxed italic">"La interfaz es tan intuitiva que incluso mis padres la usan sin dificultad. Las notificaciones nos mantienen informados de todo lo importante en tiempo real."</p>
            <div class="flex items-center gap-3 pt-4 border-t border-slate-200 dark:border-slate-700">
              <div class="w-12 h-12 rounded-full bg-gradient-to-br from-green-500 to-green-600 flex items-center justify-center text-white font-bold text-lg">MA</div>
              <div>
                <div class="font-bold text-on-surface dark:text-white">María Alejandra García</div>
                <div class="text-xs text-on-surface-variant dark:text-slate-500">Residente, Torres del Parque</div>
              </div>
            </div>
          </div>

          <!-- Testimonial 3 -->
          <div class="bg-white dark:bg-slate-800 p-8 rounded-2xl shadow-lg hover:shadow-2xl hover:-translate-y-2 transition-all border border-slate-200 dark:border-slate-700">
            <div class="flex items-center gap-1 mb-4">
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
              <span class="material-symbols-outlined text-amber-400 text-2xl">star</span>
            </div>
            <p class="text-on-surface dark:text-slate-300 mb-6 leading-relaxed italic">"El equipo de Urbansys fue excepcional durante la implementación. Sistema robusto, seguro y con un ROI que superó nuestras expectativas en el primer año."</p>
            <div class="flex items-center gap-3 pt-4 border-t border-slate-200 dark:border-slate-700">
              <div class="w-12 h-12 rounded-full bg-gradient-to-br from-purple-500 to-purple-600 flex items-center justify-center text-white font-bold text-lg">RP</div>
              <div>
                <div class="font-bold text-on-surface dark:text-white">Roberto Pérez</div>
                <div class="text-xs text-on-surface-variant dark:text-slate-500">Junta Directiva, Condominio Premium</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-24 bg-surface-container-low dark:bg-slate-900">
      <div class="max-w-7xl mx-auto px-6">
        <div class="mb-20">
          <h2 class="font-headline font-bold text-4xl text-primary dark:text-primary-fixed mb-2">Ecosistema Urbansys</h2>
          <div class="h-1 w-20 bg-tertiary-fixed rounded-full"></div>
        </div>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
          <!-- Service Card 1 -->
          <div class="group bg-gradient-to-br from-slate-50 to-slate-100 dark:from-slate-800 dark:to-slate-900 p-8 rounded-2xl transition-all hover:-translate-y-3 hover:shadow-2xl hover:shadow-blue-500/20 dark:hover:shadow-blue-500/30 border border-slate-200 dark:border-slate-700 hover:border-blue-300 dark:hover:border-blue-600 cursor-pointer">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-br from-blue-400/20 to-blue-300/20 dark:from-blue-500/30 dark:to-blue-400/20 rounded-xl blur-lg group-hover:scale-125 transition-transform duration-300"></div>
              <div class="relative bg-gradient-to-br from-blue-100 to-blue-50 dark:from-blue-900/40 dark:to-blue-800/40 w-20 h-20 rounded-xl flex items-center justify-center group-hover:scale-110 transition-transform duration-300 border-2 border-blue-200 dark:border-blue-700 shadow-md">
                <span class="material-symbols-outlined text-blue-600 dark:text-blue-300 text-5xl font-light">groups</span>
              </div>
            </div>
            <h4 class="font-headline font-bold text-lg mb-3 text-on-surface dark:text-white group-hover:text-blue-600 dark:group-hover:text-blue-300 transition-colors">Censo de Residentes</h4>
            <p class="text-sm text-on-surface-variant dark:text-slate-300 leading-relaxed">Seguimiento granular de propietarios, inquilinos y mascotas. Historial completo de propiedad a su alcance.</p>
          </div>

          <!-- Service Card 2 -->
          <div class="group bg-gradient-to-br from-slate-50 to-slate-100 dark:from-slate-800 dark:to-slate-900 p-8 rounded-2xl transition-all hover:-translate-y-3 hover:shadow-2xl hover:shadow-green-500/20 dark:hover:shadow-green-500/30 border border-slate-200 dark:border-slate-700 hover:border-green-300 dark:hover:border-green-600 cursor-pointer">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-br from-green-400/20 to-green-300/20 dark:from-green-500/30 dark:to-green-400/20 rounded-xl blur-lg group-hover:scale-125 transition-transform duration-300"></div>
              <div class="relative bg-gradient-to-br from-green-100 to-green-50 dark:from-green-900/40 dark:to-green-800/40 w-20 h-20 rounded-xl flex items-center justify-center group-hover:scale-110 transition-transform duration-300 border-2 border-green-200 dark:border-green-700 shadow-md">
                <span class="material-symbols-outlined text-green-600 dark:text-green-300 text-5xl font-light">local_parking</span>
              </div>
            </div>
            <h4 class="font-headline font-bold text-lg mb-3 text-on-surface dark:text-white group-hover:text-green-600 dark:group-hover:text-green-300 transition-colors">Hub de Parqueaderos</h4>
            <p class="text-sm text-on-surface-variant dark:text-slate-300 leading-relaxed">Gestión dinámica de vehículos, permisos de parqueo para invitados y asignación automatizada de espacios.</p>
          </div>

          <!-- Service Card 3 -->
          <div class="group bg-gradient-to-br from-slate-50 to-slate-100 dark:from-slate-800 dark:to-slate-900 p-8 rounded-2xl transition-all hover:-translate-y-3 hover:shadow-2xl hover:shadow-amber-500/20 dark:hover:shadow-amber-500/30 border border-slate-200 dark:border-slate-700 hover:border-amber-300 dark:hover:border-amber-600 cursor-pointer">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-br from-amber-400/20 to-amber-300/20 dark:from-amber-500/30 dark:to-amber-400/20 rounded-xl blur-lg group-hover:scale-125 transition-transform duration-300"></div>
              <div class="relative bg-gradient-to-br from-amber-100 to-amber-50 dark:from-amber-900/40 dark:to-amber-800/40 w-20 h-20 rounded-xl flex items-center justify-center group-hover:scale-110 transition-transform duration-300 border-2 border-amber-200 dark:border-amber-700 shadow-md">
                <span class="material-symbols-outlined text-amber-600 dark:text-amber-300 text-5xl font-light">event_available</span>
              </div>
            </div>
            <h4 class="font-headline font-bold text-lg mb-3 text-on-surface dark:text-white group-hover:text-amber-600 dark:group-hover:text-amber-300 transition-colors">Reservas</h4>
            <p class="text-sm text-on-surface-variant dark:text-slate-300 leading-relaxed">Reservas en tiempo real para zonas BBQ, gimnasio y salones de eventos con reglas de pago integradas.</p>
          </div>

          <!-- Service Card 4 -->
          <div class="group bg-gradient-to-br from-slate-50 to-slate-100 dark:from-slate-800 dark:to-slate-900 p-8 rounded-2xl transition-all hover:-translate-y-3 hover:shadow-2xl hover:shadow-pink-500/20 dark:hover:shadow-pink-500/30 border border-slate-200 dark:border-slate-700 hover:border-pink-300 dark:hover:border-pink-600 cursor-pointer">
            <div class="relative mb-6">
              <div class="absolute inset-0 bg-gradient-to-br from-pink-400/20 to-pink-300/20 dark:from-pink-500/30 dark:to-pink-400/20 rounded-xl blur-lg group-hover:scale-125 transition-transform duration-300"></div>
              <div class="relative bg-gradient-to-br from-pink-100 to-pink-50 dark:from-pink-900/40 dark:to-pink-800/40 w-20 h-20 rounded-xl flex items-center justify-center group-hover:scale-110 transition-transform duration-300 border-2 border-pink-200 dark:border-pink-700 shadow-md">
                <span class="material-symbols-outlined text-pink-600 dark:text-pink-300 text-5xl font-light">notifications_active</span>
              </div>
            </div>
            <h4 class="font-headline font-bold text-lg mb-3 text-on-surface dark:text-white group-hover:text-pink-600 dark:group-hover:text-pink-300 transition-colors">Feed Comunitario</h4>
            <p class="text-sm text-on-surface-variant dark:text-slate-300 leading-relaxed">Canal de comunicación directa. Notificaciones push para mantenimiento y reportes anuales de junta.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact & Location Section -->
    <section id="contact" class="py-24 bg-gradient-to-b from-surface-container-lowest to-slate-50 dark:from-slate-950 dark:to-slate-900 overflow-hidden">
      <div class="max-w-7xl mx-auto px-6">
        <div class="mb-20 text-center max-w-2xl mx-auto">
          <h2 class="font-headline font-bold text-5xl text-primary dark:text-blue-400 mb-4">Conecta con Nosotros</h2>
          <p class="text-lg text-on-surface-variant dark:text-slate-300">Estamos aquí para ayudarte. Envía tu consulta y nos pondremos en contacto lo antes posible.</p>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
          <!-- Contact Form Section -->
          <div class="space-y-8">
            <div class="relative">
              <div class="absolute inset-0 bg-gradient-to-r from-blue-400/10 to-purple-400/10 dark:from-blue-500/10 dark:to-purple-500/10 rounded-3xl blur-2xl"></div>
              <div class="relative bg-gradient-to-br from-white to-slate-50 dark:from-slate-800 dark:to-slate-900 p-10 rounded-2xl border border-slate-200 dark:border-slate-700 shadow-xl dark:shadow-2xl dark:shadow-blue-500/10">
                <div class="flex items-center gap-3 mb-8 pb-6 border-b border-slate-200 dark:border-slate-700">
                  <div class="w-14 h-14 rounded-full bg-gradient-to-br from-blue-500 to-blue-600 flex items-center justify-center shadow-lg">
                    <span class="material-symbols-outlined text-white text-2xl">mail</span>
                  </div>
                  <div>
                    <h3 class="font-headline font-bold text-2xl text-on-surface dark:text-white">Envía tu Mensaje</h3>
                    <p class="text-sm text-on-surface-variant dark:text-slate-400 mt-1">Responderemos en 24 horas</p>
                  </div>
                </div>
                <form class="space-y-5">
                  <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div class="space-y-2.5">
                      <label class="text-xs font-bold uppercase tracking-widest text-on-surface-variant dark:text-slate-400 block">Nombre</label>
                      <input type="text" placeholder="Tu nombre" class="w-full bg-slate-100 dark:bg-slate-700/50 border border-slate-300 dark:border-slate-600 rounded-lg px-4 py-3.5 focus:outline-none focus:ring-2 focus:ring-blue-500 dark:focus:ring-blue-400 focus:border-transparent transition-all placeholder-slate-400 dark:placeholder-slate-500 text-on-surface dark:text-white font-medium"/>
                    </div>
                    <div class="space-y-2.5">
                      <label class="text-xs font-bold uppercase tracking-widest text-on-surface-variant dark:text-slate-400 block">Apellido</label>
                      <input type="text" placeholder="Tu apellido" class="w-full bg-slate-100 dark:bg-slate-700/50 border border-slate-300 dark:border-slate-600 rounded-lg px-4 py-3.5 focus:outline-none focus:ring-2 focus:ring-blue-500 dark:focus:ring-blue-400 focus:border-transparent transition-all placeholder-slate-400 dark:placeholder-slate-500 text-on-surface dark:text-white font-medium"/>
                    </div>
                  </div>
                  <div class="space-y-2.5">
                    <label class="text-xs font-bold uppercase tracking-widest text-on-surface-variant dark:text-slate-400 block">Correo Electrónico</label>
                    <input type="email" placeholder="tu@email.com" class="w-full bg-slate-100 dark:bg-slate-700/50 border border-slate-300 dark:border-slate-600 rounded-lg px-4 py-3.5 focus:outline-none focus:ring-2 focus:ring-blue-500 dark:focus:ring-blue-400 focus:border-transparent transition-all placeholder-slate-400 dark:placeholder-slate-500 text-on-surface dark:text-white font-medium"/>
                  </div>
                  <div class="space-y-2.5">
                    <label class="text-xs font-bold uppercase tracking-widest text-on-surface-variant dark:text-slate-400 block">Teléfono (Opcional)</label>
                    <input type="tel" placeholder="+57 300 000 0000" class="w-full bg-slate-100 dark:bg-slate-700/50 border border-slate-300 dark:border-slate-600 rounded-lg px-4 py-3.5 focus:outline-none focus:ring-2 focus:ring-blue-500 dark:focus:ring-blue-400 focus:border-transparent transition-all placeholder-slate-400 dark:placeholder-slate-500 text-on-surface dark:text-white font-medium"/>
                  </div>
                  <div class="space-y-2.5">
                    <label class="text-xs font-bold uppercase tracking-widest text-on-surface-variant dark:text-slate-400 block">Asunto</label>
                    <select class="w-full bg-slate-100 dark:bg-slate-700/50 border border-slate-300 dark:border-slate-600 rounded-lg px-4 py-3.5 focus:outline-none focus:ring-2 focus:ring-blue-500 dark:focus:ring-blue-400 focus:border-transparent transition-all text-on-surface dark:text-white font-medium">
                      <option>Selecciona un asunto</option>
                      <option>Información General</option>
                      <option>Demo del Sistema</option>
                      <option>Soporte Técnico</option>
                      <option>Partnership</option>
                    </select>
                  </div>
                  <div class="space-y-2.5">
                    <label class="text-xs font-bold uppercase tracking-widest text-on-surface-variant dark:text-slate-400 block">Mensaje</label>
                    <textarea placeholder="Cuéntanos más sobre tu consulta..." class="w-full bg-slate-100 dark:bg-slate-700/50 border border-slate-300 dark:border-slate-600 rounded-lg px-4 py-3.5 focus:outline-none focus:ring-2 focus:ring-blue-500 dark:focus:ring-blue-400 focus:border-transparent transition-all placeholder-slate-400 dark:placeholder-slate-500 text-on-surface dark:text-white font-medium resize-none" rows="5"></textarea>
                  </div>
                  <button type="submit" class="w-full bg-gradient-to-r from-blue-600 to-blue-700 hover:from-blue-700 hover:to-blue-800 dark:from-blue-500 dark:to-blue-600 dark:hover:from-blue-600 dark:hover:to-blue-700 text-white py-4 rounded-xl font-bold shadow-lg hover:shadow-blue-500/40 hover:-translate-y-1 transition-all active:scale-[0.98] text-lg">
                    Enviar Consulta
                  </button>
                </form>
              </div>
            </div>
          </div>

          <!-- Map & Contact Info Section -->
          <div class="space-y-6 flex flex-col">
            <!-- Map Container -->
            <div class="relative group rounded-3xl overflow-hidden shadow-2xl dark:shadow-2xl dark:shadow-blue-500/20 border border-slate-200/60 dark:border-slate-700 flex-grow min-h-[480px]">
              <!-- Background Map with Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-blue-400 via-cyan-300 to-teal-400 dark:from-blue-900 dark:via-cyan-800 dark:to-teal-900"></div>

              <!-- Map SVG Pattern -->
              <div class="absolute inset-0 opacity-60 dark:opacity-70">
                <svg viewBox="0 0 1200 800" class="w-full h-full" preserveAspectRatio="xMidYMid slice">
                  <!-- Grid Pattern -->
                  <defs>
                    <pattern id="grid" width="60" height="60" patternUnits="userSpaceOnUse">
                      <path d="M 60 0 L 0 0 0 60" fill="none" stroke="currentColor" stroke-width="1" class="text-white/40" opacity="0.8"/>
                    </pattern>
                  </defs>
                  <rect width="1200" height="800" fill="url(#grid)" />

                  <!-- NYC Landmarks visualization -->
                  <circle cx="300" cy="250" r="15" fill="rgba(255, 255, 255, 0.7)" />
                  <circle cx="500" cy="350" r="20" fill="rgba(255, 255, 255, 0.6)" />
                  <circle cx="700" cy="200" r="18" fill="rgba(255, 255, 255, 0.65)" />
                  <circle cx="900" cy="450" r="12" fill="rgba(255, 255, 255, 0.55)" />

                  <!-- Connection lines -->
                  <line x1="300" y1="250" x2="500" y2="350" stroke="rgba(255, 255, 255, 0.5)" stroke-width="2" />
                  <line x1="500" y1="350" x2="700" y2="200" stroke="rgba(255, 255, 255, 0.5)" stroke-width="2" />
                  <line x1="700" y1="200" x2="900" y2="450" stroke="rgba(255, 255, 255, 0.5)" stroke-width="2" />
                </svg>
              </div>

              <!-- Overlay Gradient -->
              <div class="absolute inset-0 bg-gradient-to-t from-black/20 via-black/10 to-transparent dark:from-black/40 dark:via-black/20 dark:to-transparent"></div>

              <!-- Animated Background Lines -->
              <div class="absolute inset-0 overflow-hidden">
                <div class="absolute inset-0 group-hover:animate-pulse transition-all duration-500" style="background: 'linear-gradient(135deg, rgba(96, 165, 250, 0.1) 0%, transparent 50%)'"></div>
              </div>

              <!-- Map Badge -->
              <div class="absolute top-8 left-8 inline-flex items-center gap-2 px-5 py-3 rounded-full bg-gradient-to-r from-blue-600/95 to-blue-700/95 dark:from-blue-500/90 dark:to-blue-600/90 text-white text-sm font-bold tracking-wide backdrop-blur-md shadow-lg border border-white/30 hover:from-blue-700 hover:to-blue-800 dark:hover:from-blue-600 dark:hover:to-blue-700 transition-all group-hover:scale-105 group-hover:shadow-xl">
                <span class="material-symbols-outlined text-lg animate-pulse">location_on</span>
                <span>Nueva York, NY</span>
              </div>

              <!-- Location Card - MORE VISIBLE -->
              <div class="absolute bottom-8 left-8 right-8 bg-white/90 dark:bg-slate-800/90 p-8 rounded-2xl flex items-start justify-between border border-white/70 dark:border-slate-700/70 group-hover:translate-y-[-20px] transition-all duration-500 backdrop-blur-3xl shadow-2xl hover:shadow-3xl">
                <div class="flex-1">
                  <h5 class="font-headline font-bold text-2xl text-slate-900 dark:text-white mb-3 flex items-center gap-3">
                    <span class="material-symbols-outlined text-3xl bg-slate-100 dark:bg-white/30 p-2 rounded-lg text-slate-900 dark:text-white">location_on</span>
                    Sede Global
                  </h5>
                  <p class="text-base text-slate-800 dark:text-white/98 font-semibold leading-relaxed">📍 7th Avenue, Midtown Suite 400</p>
                  <p class="text-sm text-slate-700 dark:text-white/85 mt-2 font-medium">Nueva York, NY 10001</p>
                  <p class="text-xs text-slate-600 dark:text-white/70 mt-3">🕐 Disponible: Mon-Fri 9:00 AM - 6:00 PM EST</p>
                </div>
                <a href="https://www.google.com/maps/search/7th+Avenue,+Midtown+Suite+400,+New+York,+NY+10001" target="_blank" rel="noopener noreferrer" class="flex-shrink-0 bg-gradient-to-br from-blue-500 to-blue-600 dark:from-white/40 dark:to-white/20 hover:from-blue-600 hover:to-blue-700 dark:hover:from-blue-400/80 dark:hover:to-blue-500/80 text-white dark:text-white w-14 h-14 rounded-full flex items-center justify-center hover:scale-125 transition-all shadow-lg border border-blue-400/50 dark:border-white/50 hover:border-blue-300 dark:hover:border-white/70 hover:shadow-2xl">
                  <span class="material-symbols-outlined text-2xl">arrow_outward</span>
                </a>
              </div>
            </div>

            <!-- Contact Info Cards -->
            <div class="grid grid-cols-2 gap-4">
              <a href="mailto:info@urbansys.com" class="group bg-gradient-to-br from-blue-50 to-blue-100 dark:from-blue-900/30 dark:to-blue-800/40 p-6 rounded-xl border border-blue-200 dark:border-blue-700/50 hover:shadow-lg hover:-translate-y-1 transition-all hover:border-blue-400 dark:hover:border-blue-500 cursor-pointer">
                <div class="flex items-center gap-3 mb-3">
                  <span class="material-symbols-outlined text-blue-600 dark:text-blue-400 text-2xl group-hover:scale-110 transition-transform">email</span>
                  <span class="font-headline font-bold text-xs uppercase text-blue-600 dark:text-blue-400">Email</span>
                </div>
                <p class="text-sm text-on-surface dark:text-white font-medium">info@urbansys.com</p>
              </a>

              <a href="tel:+15551234567" class="group bg-gradient-to-br from-green-50 to-green-100 dark:from-green-900/30 dark:to-green-800/40 p-6 rounded-xl border border-green-200 dark:border-green-700/50 hover:shadow-lg hover:-translate-y-1 transition-all hover:border-green-400 dark:hover:border-green-500 cursor-pointer">
                <div class="flex items-center gap-3 mb-3">
                  <span class="material-symbols-outlined text-green-600 dark:text-green-400 text-2xl group-hover:scale-110 transition-transform">phone</span>
                  <span class="font-headline font-bold text-xs uppercase text-green-600 dark:text-green-400">Teléfono</span>
                </div>
                <p class="text-sm text-on-surface dark:text-white font-medium">+1 (555) 123-4567</p>
              </a>

              <div class="group bg-gradient-to-br from-purple-50 to-purple-100 dark:from-purple-900/30 dark:to-purple-800/40 p-6 rounded-xl border border-purple-200 dark:border-purple-700/50 hover:shadow-lg hover:-translate-y-1 transition-all hover:border-purple-400 dark:hover:border-purple-500 cursor-pointer">
                <div class="flex items-center gap-3 mb-3">
                  <span class="material-symbols-outlined text-purple-600 dark:text-purple-400 text-2xl group-hover:scale-110 transition-transform">schedule</span>
                  <span class="font-headline font-bold text-xs uppercase text-purple-600 dark:text-purple-400">Horarios</span>
                </div>
                <p class="text-sm text-on-surface dark:text-white font-medium">Lun - Vie 9:00 - 18:00</p>
              </div>

              <a href="https://www.urbansys.com" target="_blank" class="group bg-gradient-to-br from-orange-50 to-orange-100 dark:from-orange-900/30 dark:to-orange-800/40 p-6 rounded-xl border border-orange-200 dark:border-orange-700/50 hover:shadow-lg hover:-translate-y-1 transition-all hover:border-orange-400 dark:hover:border-orange-500 cursor-pointer">
                <div class="flex items-center gap-3 mb-3">
                  <span class="material-symbols-outlined text-orange-600 dark:text-orange-400 text-2xl group-hover:scale-110 transition-transform">public</span>
                  <span class="font-headline font-bold text-xs uppercase text-orange-600 dark:text-orange-400">Web</span>
                </div>
                <p class="text-sm text-on-surface dark:text-white font-medium">www.urbansys.com</p>
              </a>
            </div>

            <!-- Social Links -->
            <div class="flex justify-center gap-4 pt-6">
              <a href="https://www.linkedin.com" target="_blank" class="group w-12 h-12 rounded-full bg-gradient-to-br from-slate-100 to-slate-200 dark:from-slate-700 dark:to-slate-800 hover:from-blue-500 hover:to-blue-600 dark:hover:from-blue-600 dark:hover:to-blue-700 text-slate-600 dark:text-slate-400 hover:text-white transition-all flex items-center justify-center shadow-md hover:shadow-lg hover:scale-110 duration-300 border border-slate-200 dark:border-slate-700">
                <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" fill="currentColor" aria-hidden="true">
                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                </svg>
              </a>
              <a href="https://www.facebook.com" target="_blank" class="group w-12 h-12 rounded-full bg-gradient-to-br from-slate-100 to-slate-200 dark:from-slate-700 dark:to-slate-800 hover:from-blue-500 hover:to-blue-600 dark:hover:from-blue-600 dark:hover:to-blue-700 text-slate-600 dark:text-slate-400 hover:text-white transition-all flex items-center justify-center shadow-md hover:shadow-lg hover:scale-110 duration-300 border border-slate-200 dark:border-slate-700">
                <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" fill="currentColor" aria-hidden="true">
                  <path d="M9.101 23.691v-7.98H6.627v-3.667h2.474v-1.58c0-4.085 1.848-5.978 5.858-5.978.401 0 .955.042 1.468.103a8.68 8.68 0 0 1 1.141.195v3.325a8.623 8.623 0 0 0-.653-.036 26.805 26.805 0 0 0-.733-.009c-.707 0-1.259.096-1.675.309a1.686 1.686 0 0 0-.679.622c-.258.42-.374.995-.374 1.752v1.297h3.919l-.386 2.103-.287 1.564h-3.246v8.245C19.396 23.238 24 18.179 24 12.044c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.628 3.874 10.35 9.101 11.647Z"/>
                </svg>
              </a>
              <a href="mailto:info@urbansys.com" class="group w-12 h-12 rounded-full bg-gradient-to-br from-slate-100 to-slate-200 dark:from-slate-700 dark:to-slate-800 hover:from-blue-500 hover:to-blue-600 dark:hover:from-blue-600 dark:hover:to-blue-700 text-slate-600 dark:text-slate-400 hover:text-white transition-all flex items-center justify-center shadow-md hover:shadow-lg hover:scale-110 duration-300 border border-slate-200 dark:border-slate-700">
                <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" fill="currentColor" aria-hidden="true">
                  <path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/>
                </svg>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- WhatsApp Floating CTA -->
  <a href="https://wa.me/?text=Hola%20me%20gustar%C3%ADa%20m%C3%A1s%20informaci%C3%B3n%20sobre%20System%20Urbansys" target="_blank" rel="noopener noreferrer" class="fixed bottom-4 right-4 sm:bottom-6 sm:right-6 md:bottom-8 md:right-8 group z-40">
    <div class="absolute -left-48 sm:-left-56 top-1/2 sm:top-auto sm:-top-20 -translate-y-1/2 sm:translate-y-0 bg-gradient-to-r from-slate-900 via-slate-800 to-slate-800 dark:from-slate-700 dark:via-slate-600 dark:to-slate-700 text-white px-4 sm:px-6 py-3 sm:py-4 rounded-xl text-xs sm:text-sm font-bold shadow-2xl shadow-slate-900/50 opacity-0 group-hover:opacity-100 transition-all duration-300 pointer-events-none border border-slate-700 dark:border-slate-500 whitespace-nowrap">
      <div class="flex items-center gap-2">
        <span class="inline-flex items-center justify-center text-lg sm:text-xl animate-bounce">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" class="w-4 sm:w-5 h-4 sm:h-5" fill="currentColor" aria-hidden="true">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884"/>
          </svg>
        </span>
        Chatea con nosotros
      </div>
      <div class="hidden sm:block absolute left-full top-1/2 -translate-y-1/2 w-3 h-3 bg-slate-800 dark:bg-slate-600 rotate-45 border-r border-b border-slate-700 dark:border-slate-500"></div>
      <div class="sm:hidden absolute left-1/2 -translate-x-1/2 top-full w-3 h-3 bg-slate-800 dark:bg-slate-600 rotate-45 border-l border-t border-slate-700 dark:border-slate-500 mt-1"></div>
    </div>
    <div class="relative inline-flex items-center justify-center bg-gradient-to-br from-green-400 via-green-500 to-green-600 hover:from-green-500 hover:via-green-600 hover:to-green-700 text-white rounded-full shadow-2xl hover:shadow-green-500/60 hover:scale-110 group-hover:-rotate-12 transition-all duration-300 active:scale-95 border border-green-300/50 hover:border-green-200" style="width: fit-content; height: fit-content;">
      <button class="relative w-12 sm:w-14 md:w-16 h-12 sm:h-14 md:h-16 p-3 sm:p-4 md:p-5 rounded-full flex items-center justify-center" style="aspect-ratio: 1 / 1;">
        <div class="absolute inset-0 rounded-full bg-black/15 dark:bg-white/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300 animate-pulse"></div>
        <div class="absolute inset-2 rounded-full border-2 border-black/15 dark:border-white/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300 animate-ping"></div>
        <span class="relative z-10 inline-flex items-center justify-center">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" class="w-5 sm:w-6 md:w-7 h-5 sm:h-6 md:h-7" fill="currentColor" aria-hidden="true">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884"/>
          </svg>
        </span>
      </button>
    </div>
  </a>

  <!-- Footer -->
  <footer class="w-full border-t border-slate-200/50 dark:border-slate-800 bg-gradient-to-br from-slate-50 to-slate-100 dark:from-slate-950 dark:to-slate-900 transition-colors duration-300">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 px-8 py-12 max-w-7xl mx-auto text-center md:text-left">
      <div class="md:col-span-1">
        <div class="text-2xl font-extrabold text-blue-900 dark:text-blue-400 mb-4 font-headline">System Urbansys</div>
        <p class="text-sm leading-relaxed text-slate-600 dark:text-slate-400 max-w-xs mx-auto md:mx-0">
          Arquitectando el futuro de las comunidades residenciales con precisión y elegancia.
        </p>
      </div>
      <div class="grid grid-cols-2 sm:grid-cols-3 gap-8">
        <div>
          <h6 class="font-headline font-bold text-blue-900 dark:text-blue-400 mb-4 text-xs uppercase tracking-widest">Plataforma</h6>
          <ul class="space-y-2 text-sm leading-relaxed">
            <li><a href="#services" class="text-slate-600 dark:text-slate-400 hover:text-blue-700 dark:hover:text-blue-300 underline-offset-4 hover:underline transition-all">Censo Residencial</a></li>
            <li><a href="#services" class="text-slate-600 dark:text-slate-400 hover:text-blue-700 dark:hover:text-blue-300 underline-offset-4 hover:underline transition-all">Parqueaderos</a></li>
            <li><a href="#services" class="text-slate-600 dark:text-slate-400 hover:text-blue-700 dark:hover:text-blue-300 underline-offset-4 hover:underline transition-all">Reservas</a></li>
          </ul>
        </div>
        <div>
          <h6 class="font-headline font-bold text-blue-900 dark:text-blue-400 mb-4 text-xs uppercase tracking-widest">Empresa</h6>
          <ul class="space-y-2 text-sm leading-relaxed">
            <li><a href="#mission" class="text-slate-600 dark:text-slate-400 hover:text-blue-700 dark:hover:text-blue-300 underline-offset-4 hover:underline transition-all">Misión</a></li>
            <li><a href="#" class="text-slate-600 dark:text-slate-400 hover:text-blue-700 dark:hover:text-blue-300 underline-offset-4 hover:underline transition-all">Privacidad</a></li>
            <li><a href="#" class="text-slate-600 dark:text-slate-400 hover:text-blue-700 dark:hover:text-blue-300 underline-offset-4 hover:underline transition-all">Términos</a></li>
          </ul>
        </div>
        <div class="hidden sm:block">
          <h6 class="font-headline font-bold text-blue-900 dark:text-blue-400 mb-4 text-xs uppercase tracking-widest">Soporte</h6>
          <ul class="space-y-2 text-sm leading-relaxed">
            <li><a href="#" class="text-slate-600 dark:text-slate-400 hover:text-blue-700 dark:hover:text-blue-300 underline-offset-4 hover:underline transition-all">Ayuda</a></li>
            <li><a href="#contact" class="text-slate-600 dark:text-slate-400 hover:text-blue-700 dark:hover:text-blue-300 underline-offset-4 hover:underline transition-all">Contacto</a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="max-w-7xl mx-auto px-6 py-8 border-t border-slate-200/50 dark:border-slate-800 flex flex-col md:flex-row justify-between items-center gap-4">
      <span class="text-xs text-slate-600 dark:text-slate-500">© 2024 System Urbansys. Excelencia Arquitectónica.</span>
      <div class="flex gap-8">
        <a href="#" class="text-xs text-slate-600 dark:text-slate-500 hover:text-blue-700 dark:hover:text-blue-300 transition-colors">Cookies</a>
        <a href="#" class="text-xs text-slate-600 dark:text-slate-500 hover:text-blue-700 dark:hover:text-blue-300 transition-colors">Soporte</a>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.glass-panel {
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border-radius: 12px;
}

.dark .glass-panel {
  background: rgba(30, 41, 59, 0.85);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
}

/* Smooth scrolling enhancement */
html {
  scroll-behavior: smooth;
}

/* Animation for bounce effect */
@keyframes bounce-soft {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-8px);
  }
}

/* Ping animation */
@keyframes ping {
  75%, 100% {
    transform: scale(2);
    opacity: 0;
  }
}

.animate-bounce {
  animation: bounce-soft 2s infinite;
}

.animate-ping {
  animation: ping 2s cubic-bezier(0, 0, 0.2, 1) infinite;
}
</style>
