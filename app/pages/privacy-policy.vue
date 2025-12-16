<template>
  <div class="min-h-screen bg-white">
    <div class="max-w-4xl mx-auto px-4 md:px-12 py-20">
      <h1 class="text-4xl font-bold text-slate-900 mb-8">Политика конфиденциальности</h1>
      
      <div class="prose prose-slate max-w-none">
        <p class="text-slate-600 mb-6">
          <strong>Дата последнего обновления:</strong> {{ new Date().toLocaleDateString('ru-RU') }}
        </p>

        <section class="mb-8">
          <h2 class="text-2xl font-semibold text-slate-900 mb-4">1. Общие положения</h2>
          <p class="text-slate-600 mb-4">
            Настоящая Политика конфиденциальности определяет порядок обработки и защиты персональных данных 
            пользователей веб-сайта SaltaCRM (далее — «Сайт»). Используя Сайт, вы соглашаетесь с условиями 
            настоящей Политики конфиденциальности.
          </p>
        </section>

        <section class="mb-8">
          <h2 class="text-2xl font-semibold text-slate-900 mb-4">2. Собираемая информация</h2>
          <p class="text-slate-600 mb-4">
            Мы можем собирать следующую информацию:
          </p>
          <ul class="list-disc pl-6 text-slate-600 mb-4">
            <li>Имя и контактная информация</li>
            <li>Адрес электронной почты</li>
            <li>Информация об использовании Сайта</li>
            <li>Технические данные (IP-адрес, тип браузера, операционная система)</li>
          </ul>
        </section>

        <section class="mb-8">
          <h2 class="text-2xl font-semibold text-slate-900 mb-4">3. Использование информации</h2>
          <p class="text-slate-600 mb-4">
            Собранная информация используется для:
          </p>
          <ul class="list-disc pl-6 text-slate-600 mb-4">
            <li>Предоставления и улучшения наших услуг</li>
            <li>Обработки ваших запросов и обращений</li>
            <li>Отправки информационных материалов (с вашего согласия)</li>
            <li>Обеспечения безопасности и предотвращения мошенничества</li>
          </ul>
        </section>

        <section class="mb-8">
          <h2 class="text-2xl font-semibold text-slate-900 mb-4">4. Защита данных</h2>
          <p class="text-slate-600 mb-4">
            Мы применяем современные методы защиты информации для обеспечения безопасности ваших 
            персональных данных от несанкционированного доступа, изменения, раскрытия или уничтожения.
          </p>
        </section>

        <section class="mb-8">
          <h2 class="text-2xl font-semibold text-slate-900 mb-4">5. Передача данных третьим лицам</h2>
          <p class="text-slate-600 mb-4">
            Мы не продаем, не обмениваем и не передаем ваши персональные данные третьим лицам без 
            вашего согласия, за исключением случаев, предусмотренных законодательством.
          </p>
        </section>

        <section class="mb-8">
          <h2 class="text-2xl font-semibold text-slate-900 mb-4">6. Ваши права</h2>
          <p class="text-slate-600 mb-4">
            Вы имеете право:
          </p>
          <ul class="list-disc pl-6 text-slate-600 mb-4">
            <li>Получать информацию о ваших персональных данных</li>
            <li>Требовать исправления неточных данных</li>
            <li>Требовать удаления ваших персональных данных</li>
            <li>Отозвать согласие на обработку персональных данных</li>
          </ul>
        </section>

        <section class="mb-8">
          <h2 class="text-2xl font-semibold text-slate-900 mb-4">7. Контакты</h2>
          <p class="text-slate-600 mb-4">
            По всем вопросам, связанным с обработкой персональных данных, вы можете обращаться 
            по адресу электронной почты, указанному в разделе «Контакты» на Сайте.
          </p>
        </section>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Политика конфиденциальности',
  meta: [
    {
      name: 'description',
      content: 'Политика конфиденциальности SaltaCRM - информация о сборе, использовании и защите персональных данных'
    }
  ]
})
</script>
