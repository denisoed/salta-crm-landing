<template>
  <section class="py-20 px-4">
    <div class="max-w-6xl mx-auto">
      <div class="bg-white rounded-[2rem] shadow-2xl shadow-slate-200 border border-slate-200 p-2 md:p-4 overflow-hidden relative">
        <div class="flex items-center gap-2 px-4 py-3 border-b border-slate-100 bg-slate-50/50 rounded-t-xl mb-4">
          <div class="w-3 h-3 rounded-full bg-red-400" />
          <div class="w-3 h-3 rounded-full bg-yellow-400" />
          <div class="w-3 h-3 rounded-full bg-green-400" />
          <div
            class="ml-4 bg-white px-3 py-1 rounded text-xs text-slate-400 border border-slate-200 flex-1 max-w-xs text-center"
          >
            app.saltacrm.com
          </div>
        </div>

        <div class="grid md:grid-cols-12 gap-6 p-4">
          <div class="hidden md:block col-span-2 space-y-2">
            <div class="h-10 w-full bg-blue-50 text-blue-600 rounded-lg flex items-center px-3 font-bold text-sm">
              Главная
            </div>
            <div class="h-10 w-full hover:bg-slate-50 rounded-lg flex items-center px-3 text-slate-500 text-sm">
              Заказы
            </div>
            <div class="h-10 w-full hover:bg-slate-50 rounded-lg flex items-center px-3 text-slate-500 text-sm">
              Склад
            </div>
          </div>

          <div class="col-span-12 md:col-span-10 space-y-6">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
              <div class="p-6 rounded-2xl bg-white border border-slate-100 shadow-sm">
                <div class="text-sm text-slate-400 mb-1">Выручка за сегодня</div>
                <div class="text-3xl font-bold text-slate-900">42 000 ₽</div>
              </div>
              <div class="p-6 rounded-2xl bg-white border border-slate-100 shadow-sm">
                <div class="text-sm text-slate-400 mb-1">Новых заказов</div>
                <div class="text-3xl font-bold text-blue-600">12</div>
              </div>
              <div class="p-6 rounded-2xl bg-white border border-slate-100 shadow-sm">
                <div class="text-sm text-slate-400 mb-1">Товаров заканчивается</div>
                <div class="text-3xl font-bold text-red-500">3</div>
              </div>
            </div>

            <div class="rounded-2xl border border-slate-100 overflow-hidden">
              <div class="px-6 py-4 border-b border-slate-100 bg-slate-50/50 flex justify-between">
                <span class="font-bold text-slate-700">Последние заказы</span>
                <span class="text-blue-600 text-sm font-semibold cursor-pointer">Все заказы &rarr;</span>
              </div>
              <div class="divide-y divide-slate-50 bg-white">
                <div class="px-6 py-4 flex items-center justify-between hover:bg-slate-50 transition-colors">
                  <div class="flex items-center gap-4">
                    <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-slate-500">AI</div>
                    <div>
                      <div class="font-bold text-slate-900">Алексей Иванов</div>
                      <div class="text-xs text-slate-400">Кроссовки Nike Air • 1 шт</div>
                    </div>
                  </div>
                  <span class="px-3 py-1 rounded-full bg-green-100 text-green-700 text-xs font-bold">Оплачен</span>
                </div>
                <div class="px-6 py-4 flex items-center justify-between hover:bg-slate-50 transition-colors">
                  <div class="flex items-center gap-4">
                    <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-slate-500">MK</div>
                    <div>
                      <div class="font-bold text-slate-900">Мария К.</div>
                      <div class="text-xs text-slate-400">Платье летнее • 2 шт</div>
                    </div>
                  </div>
                  <span class="px-3 py-1 rounded-full bg-blue-100 text-blue-700 text-xs font-bold">Новый</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>


