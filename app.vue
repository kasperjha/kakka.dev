<template>
  <div class="flex w-full justify-center">


    <section
      class="max-w-xl w-full flex flex-col min-h-screen px-4 sm:px-8 leading-relaxed font-mono text-gray-900 break-words">
      <nav class="mt-6 mb-4">
        <div class="flex gap-x-4">
          <NavItem destination="/" name="kakka.dev" class="font-bold mr-auto" />
          <NavItem destination="/now/" name="now" />
          <NavItem destination="/work/" name="work" />
          <NavItem destination="/contact/" name="contact" />
          <NavItem destination="https://plausible.kakk.dev/kakka.dev" name="stats" external class="hidden sm:block" />
        </div>
      </nav>
      <main class="flex-grow pt-10 pb-20">
        <NuxtPage />
      </main>
      <footer class="flex justify-center py-4 text-xs italic text-gray-700">
        <p>
          Developed with <a href="https://nuxtjs.org">Nuxt</a>,
          <a href="https://nuxtjs.org">Vue</a> and
          <a href="https://tailwindcss.com">Tailwind</a>. View <a href="https://github.com/kasperjha/kakka.dev">on
            GitHub</a>.
        </p>
      </footer>
    </section>
  </div>
</template>

<style>
.page-enter-active,
.page-leave-active {
  transition: all 200ms;
}

.page-enter-from,
.page-leave-to {
  opacity: 0;
  filter: blur(5px);
  transform: translateY(5px);
}

body {
  --dot-bg: white;
  --dot-color: gray;
  --dot-size: 1px;
  --dot-space: 20px;
  background:
    linear-gradient(90deg, var(--dot-bg) calc(var(--dot-space) - var(--dot-size)), transparent 1%) center / var(--dot-space) var(--dot-space),
    linear-gradient(var(--dot-bg) calc(var(--dot-space) - var(--dot-size)), transparent 1%) center / var(--dot-space) var(--dot-space),
    var(--dot-color);
}

p a {
  text-decoration: underline;
  color: blue;
}

p a:hover {
  color: red;
}
</style>

<script setup>
useHead({
  script: [
    { defer: 'defer', src: 'https://plausible.kakk.dev/js/plausible.js', 'data-domain': 'kakka.dev' }
  ],
  link: [
    { rel: 'icon', type: 'image/x-icon', href: 'favicon.ico' }
  ],
  meta: [{ name: 'description', content: 'Heyo! I\'m Kasper. Check out my portfolio: During daytime i study for a CompSci degree, and on the side i enjoy building ool websites for cool people.' }]
})

useSeoMeta({
  title: 'kakka.dev',
  ogTitle: 'kakka.dev',
  description: 'I\'m a freelance software developer, web designer and soon to be Computer Science graduate. Check out my projects, freelance availability and whats been my focus recently',
  ogDescription: 'I\'m a freelance software developer, web designer and soon to be Computer Science graduate.',
  ogImage: '/me.jpeg'
})
</script>
