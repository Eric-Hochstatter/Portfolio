// app.vue
<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup lang="ts">
useHead({
  title: "Portfolio von Eric Hochstatter",
  meta: [{ name: "description", content: "Portfolio von Eric Hochstatter - Interaktionsdesign Student" }],
  htmlAttrs: {
    lang: "de",
  },
  link: [
    {
      rel: "icon",
      type: "image/png",
      href: "/favicon.png",
    },
  ],
});

useSeoMeta({
  description: "Portfolio von Eric Hochstatter - Interaktionsdesign Student",
  ogTitle: "Portfolio von Eric Hochstatter",
  ogDescription:
    "Hier findest du mehr über meine Design-Projekte, meinen Arbeitsprozess und meine Fähigkeiten.",
  ogImage: "/og-image.png",
  ogUrl: "https://erichochstatter.com",
  twitterTitle: "Portfolio von Eric Hochstatter",
  twitterDescription: "Portfolio von Eric Hochstatter - Interaktionsdesign Student",
  twitterImage: "/og-image.png",
  twitterCard: "summary",
});
</script>