<template>
  <nav
    class="fixed top-0 w-full z-50 py-4 px-6 md:px-12 transition-all duration-300 bg-white/70 backdrop-blur-md border-b border-slate-100"
  >
    <div class="max-w-7xl mx-auto flex justify-between items-center">
      <NuxtLink to="/" class="flex items-center gap-2">
        <div class="w-8 h-8 bg-slate-900 rounded-lg flex items-center justify-center text-white font-bold">
          S
        </div>
        <span class="font-bold text-xl text-slate-900 tracking-tight">SaltaCRM</span>
      </NuxtLink>

      <div class="hidden md:flex gap-8 text-sm font-semibold text-slate-500">
        <NuxtLink to="/#about" class="hover:text-blue-600 transition-colors">О продукте</NuxtLink>
        <NuxtLink to="/#solutions" class="hover:text-blue-600 transition-colors">Решения</NuxtLink>
        <NuxtLink to="/#ai" class="hover:text-blue-600 transition-colors">Технологии</NuxtLink>
      </div>

      <div class="flex gap-4">
        <button class="hidden md:block text-slate-600 font-semibold text-sm hover:text-slate-900" type="button">
          Войти
        </button>
        <button
          class="bg-slate-900 text-white px-5 py-2.5 rounded-lg font-semibold text-sm hover:bg-slate-800 transition-all shadow-lg shadow-slate-200"
          type="button"
        >
          Регистрация
        </button>
      </div>
    </div>
  </nav>
</template>


