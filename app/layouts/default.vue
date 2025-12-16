<template>
  <div>
    <ClientOnly>
      <ThreeBackground />
    </ClientOnly>

    <AppNav />
    <main>
      <slot />
    </main>
    <AppFooter />
  </div>
</template>

<script setup lang="ts">
useHead({
  htmlAttrs: { lang: 'ru' },
  titleTemplate: (titleChunk) => (titleChunk ? `${titleChunk} · SaltaCRM` : 'SaltaCRM - Чистота и Порядок'),
  meta: [
    { charset: 'utf-8' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1.0' },
  ],
  link: [
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap',
    },
  ],
  script: [
    // Tailwind via CDN (no local dependency in this repo yet)
    { src: 'https://cdn.tailwindcss.com', defer: true },
  ],
  style: [
    {
      children: `
html { scroll-behavior: smooth; }
body {
  font-family: 'Plus Jakarta Sans', sans-serif;
  background-color: #ffffff;
  color: #0f172a;
  overflow-x: hidden;
}
.soft-card {
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border: 1px solid rgba(226, 232, 240, 0.8);
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.02), 0 2px 4px -1px rgba(0, 0, 0, 0.02);
  transition: all 0.3s ease;
}
.soft-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.05), 0 10px 10px -5px rgba(0, 0, 0, 0.01);
  border-color: #3b82f6;
}
      `.trim(),
    },
  ],
})
</script>


