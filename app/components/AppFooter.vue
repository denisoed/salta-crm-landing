<template>
  <footer class="bg-white pt-20 pb-10 border-t border-slate-100">
    <div class="max-w-7xl mx-auto px-4 md:px-12">
      <div class="flex flex-col md:flex-row justify-between items-center mb-12">
        <AppBrandLink class="mb-6 md:mb-0" />

        <div class="flex gap-8 text-sm text-slate-600 font-medium">
          <NuxtLink to="/#about" class="hover:text-blue-600">О нас</NuxtLink>
          <NuxtLink to="/#solutions" class="hover:text-blue-600">Тарифы</NuxtLink>
          <NuxtLink to="/#about" class="hover:text-blue-600">Контакты</NuxtLink>
        </div>
      </div>

      <div class="flex flex-col md:flex-row justify-between items-center pt-8 border-t border-slate-50 text-xs text-slate-400">
        <p>&copy; 2024 SaltaCRM Inc. Сделано с любовью к порядку.</p>
        <div class="flex gap-4 mt-4 md:mt-0">
          <NuxtLink to="/#about" class="hover:text-slate-600">Политика конфиденциальности</NuxtLink>
          <NuxtLink to="/#about" class="hover:text-slate-600">Условия использования</NuxtLink>
        </div>
      </div>
    </div>
  </footer>
</template>


