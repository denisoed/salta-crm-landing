<template>
  <section class="min-h-screen flex items-center justify-center pt-20 px-4 relative">
    <div class="max-w-5xl mx-auto text-center z-10">
      <div
        class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-blue-50 border border-blue-100 text-blue-600 text-xs font-bold uppercase tracking-wide mb-8"
      >
        <span class="relative flex h-2 w-2">
          <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-blue-400 opacity-75" />
          <span class="relative inline-flex rounded-full h-2 w-2 bg-blue-500" />
        </span>
        Новый стандарт управления
      </div>

      <h1 class="text-6xl md:text-8xl font-extrabold mb-8 tracking-tight text-slate-900 leading-[1.1]">
        Бизнес без <br />
        <span class="text-blue-600">лишнего шума</span>
      </h1>

      <p class="text-xl max-w-2xl mx-auto mb-10 leading-relaxed font-light">
        Мы убрали всё лишнее, оставив только то, что приносит деньги. Учет, склад и AI-аналитика в кристально чистом
        интерфейсе.
      </p>

      <div class="flex flex-col sm:flex-row justify-center gap-4">
        <button
          class="bg-blue-600 text-white px-8 py-4 rounded-xl font-bold text-lg hover:bg-blue-700 transition-all shadow-xl shadow-blue-200 hover:-translate-y-1"
          type="button"
        >
          Попробовать бесплатно
        </button>
        <NuxtLink
          to="/#ai"
          class="bg-white text-slate-700 border border-slate-200 px-8 py-4 rounded-xl font-bold text-lg hover:bg-slate-50 transition-all flex items-center justify-center gap-2"
        >
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M14.752 11.168l-3.197-2.132A1 1 0 0010 9.87v4.263a1 1 0 001.555.832l3.197-2.132a1 1 0 000-1.664z"
            />
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
            />
          </svg>
          Как это работает
        </NuxtLink>
      </div>

      <div class="mt-16 grid grid-cols-2 md:grid-cols-4 gap-8 border-t border-slate-100 pt-8 max-w-3xl mx-auto opacity-70">
        <div>
          <div class="text-3xl font-bold text-slate-900">2 мин</div>
          <div class="text-sm text-slate-500">На запуск</div>
        </div>
        <div>
          <div class="text-3xl font-bold text-slate-900">0 ₽</div>
          <div class="text-sm text-slate-500">На старте</div>
        </div>
        <div>
          <div class="text-3xl font-bold text-slate-900">AI</div>
          <div class="text-sm text-slate-500">Ассистент</div>
        </div>
        <div>
          <div class="text-3xl font-bold text-slate-900">24/7</div>
          <div class="text-sm text-slate-500">Доступ</div>
        </div>
      </div>
    </div>
  </section>
</template>


