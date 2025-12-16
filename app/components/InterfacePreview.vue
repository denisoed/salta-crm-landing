<template>
  <section id="about" class="py-24 px-4 scroll-mt-24">
    <div class="max-w-6xl mx-auto">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <div>
          <div
            class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-blue-50 border border-blue-100 text-blue-600 text-xs font-bold uppercase tracking-wide mb-6"
          >
            О продукте
          </div>

          <h2 class="text-3xl md:text-4xl font-bold mb-4 text-slate-900">
            SaltaCRM — порядок в продажах, складе и финансах
          </h2>

          <p class="text-slate-500 leading-relaxed mb-8 bg-white/70 backdrop-blur-md rounded-xl px-6 py-4 border border-slate-100">
            Всё, что обычно живёт в таблицах, чатах и голове — собирается в одной системе: заказы, остатки, статусы, оплаты и
            контроль. Без перегруза интерфейсом и “сложных настроек”.
          </p>

          <div class="grid sm:grid-cols-2 gap-4 mb-10">
            <div class="soft-card p-5 rounded-2xl bg-white">
              <div class="flex items-start gap-3">
                <div class="w-10 min-w-10 h-10 rounded-xl bg-blue-100 text-blue-600 flex items-center justify-center">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 22C6.477 22 2 17.523 2 12S6.477 2 12 2s10 4.477 10 10-4.477 10-10 10z" />
                  </svg>
                </div>
                <div>
                  <div class="font-bold text-slate-900">Быстрый запуск</div>
                  <div class="text-sm text-slate-500">Начните вести заказы и склад за пару минут.</div>
                </div>
              </div>
            </div>

            <div class="soft-card p-5 rounded-2xl bg-white">
              <div class="flex items-start gap-3">
                <div class="w-10 min-w-10 h-10 rounded-xl bg-emerald-100 text-emerald-700 flex items-center justify-center">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 7h18M3 12h18M3 17h18" />
                  </svg>
                </div>
                <div>
                  <div class="font-bold text-slate-900">Единый контур</div>
                  <div class="text-sm text-slate-500">Склад ↔ заказы ↔ деньги — всё связано.</div>
                </div>
              </div>
            </div>

            <div class="soft-card p-5 rounded-2xl bg-white">
              <div class="flex items-start gap-3">
                <div class="w-10 min-w-10 h-10 rounded-xl bg-amber-100 text-amber-700 flex items-center justify-center">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                  </svg>
                </div>
                <div>
                  <div class="font-bold text-slate-900">Скорость команды</div>
                  <div class="text-sm text-slate-500">Статусы, ответственные, история — без хаоса.</div>
                </div>
              </div>
            </div>

            <div class="soft-card p-5 rounded-2xl bg-white">
              <div class="flex items-start gap-3">
                <div class="w-10 min-w-10 h-10 rounded-xl bg-purple-100 text-purple-700 flex items-center justify-center">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1" />
                  </svg>
                </div>
                <div>
                  <div class="font-bold text-slate-900">Понятные цифры</div>
                  <div class="text-sm text-slate-500">Выручка, маржа, остатки — без “магии” в таблицах.</div>
                </div>
              </div>
            </div>
          </div>

          <div class="flex flex-col sm:flex-row gap-4">
            <button
              class="bg-blue-600 text-white px-8 py-4 rounded-xl font-bold text-base hover:bg-blue-700 transition-all shadow-xl shadow-blue-200 hover:-translate-y-1"
              type="button"
            >
              Попробовать бесплатно
            </button>
            <NuxtLink
              to="/#solutions"
              class="bg-white text-slate-700 border border-slate-200 px-8 py-4 rounded-xl font-bold text-base hover:bg-slate-50 transition-all flex items-center justify-center gap-2"
            >
              Смотреть решения
              <span aria-hidden="true">&rarr;</span>
            </NuxtLink>
          </div>
        </div>

        <div class="relative">
          <div class="bg-white rounded-[2rem] border border-slate-200 p-2 md:p-4 overflow-hidden soft-card">
            <div class="flex items-center gap-2 px-4 py-3 border-b border-slate-100 bg-slate-50/50 rounded-t-xl">
              <div class="w-3 h-3 rounded-full bg-red-400" />
              <div class="w-3 h-3 rounded-full bg-yellow-400" />
              <div class="w-3 h-3 rounded-full bg-green-400" />
              <div class="ml-4 bg-white px-3 py-1 rounded text-xs text-slate-400 border border-slate-200 flex-1 max-w-xs text-center">
                salta — overview
              </div>
            </div>

            <div class="p-4 md:p-6 space-y-4">
              <div class="grid grid-cols-2 gap-4">
                <div class="p-5 rounded-2xl bg-white border border-slate-100 shadow-sm">
                  <div class="text-xs text-slate-400 mb-1">Заказы в работе</div>
                  <div class="text-2xl font-extrabold text-slate-900">18</div>
                  <div class="text-xs text-slate-400 mt-1">+4 за сутки</div>
                </div>
                <div class="p-5 rounded-2xl bg-white border border-slate-100 shadow-sm">
                  <div class="text-xs text-slate-400 mb-1">Остатки на складе</div>
                  <div class="text-2xl font-extrabold text-blue-600">246</div>
                  <div class="text-xs text-slate-400 mt-1">SKU</div>
                </div>
              </div>

              <div class="grid grid-cols-3 gap-4">
                <div class="p-5 rounded-2xl bg-white border border-slate-100 shadow-sm">
                  <div class="text-xs text-slate-400 mb-1">Выручка</div>
                  <div class="text-lg font-extrabold text-slate-900">1.2M ₽</div>
                </div>
                <div class="p-5 rounded-2xl bg-white border border-slate-100 shadow-sm">
                  <div class="text-xs text-slate-400 mb-1">Маржа</div>
                  <div class="text-lg font-extrabold text-emerald-700">24%</div>
                </div>
                <div class="p-5 rounded-2xl bg-white border border-slate-100 shadow-sm">
                  <div class="text-xs text-slate-400 mb-1">Риски</div>
                  <div class="text-lg font-extrabold text-amber-700">2</div>
                </div>
              </div>

              <div class="rounded-2xl border border-slate-100 overflow-hidden bg-white">
                <div class="px-5 py-4 border-b border-slate-100 bg-slate-50/50 flex items-center justify-between">
                  <span class="font-bold text-slate-700">Подсказки AI</span>
                  <span class="text-blue-600 text-xs font-semibold">Подробнее</span>
                </div>
                <div class="p-5 space-y-3">
                  <div class="flex items-start gap-3">
                    <div class="w-9 min-w-9 h-9 rounded-full bg-blue-100 text-blue-700 flex items-center justify-center font-bold text-xs">
                      AI
                    </div>
                    <div class="text-sm text-slate-600 leading-relaxed">
                      По товару “Кроссовки” заканчивается размер 42 — стоит докупить 6 шт, чтобы не терять продажи.
                    </div>
                  </div>
                  <div class="flex items-start gap-3">
                    <div class="w-9 min-w-9 h-9 rounded-full bg-slate-100 text-slate-600 flex items-center justify-center font-bold text-xs">
                      AI
                    </div>
                    <div class="text-sm text-slate-600 leading-relaxed">
                      Доставка по заказам #1042 и #1047 задерживается — проверьте статус у перевозчика.
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
