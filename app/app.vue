<script setup lang="ts">
useHead({
  meta: [
    { name: "viewport", content: "width=device-width, initial-scale=1" },
  ],
  link: [
    { rel: "icon", href: "/favicon.ico" },
  ],
  htmlAttrs: {
    lang: "en",
  },
});

const title = "Stackhacker UI Starter Template";
const description = "A production-ready starter template powered by Nuxt 4, shadcn-vue, and Tailwind CSS v4.";

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: "https://ui.stackhacker.io/templates/starter-light.png",
  twitterCard: "summary_large_image",
});
</script>

<template>
  <div class="min-h-screen bg-background text-foreground">
    <SiteHeader />

    <main class="border-grid border-y">
      <NuxtPage />
    </main>

    <SiteFooter />
  </div>
</template>
