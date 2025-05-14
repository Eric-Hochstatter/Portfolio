// components/NavButtons.vue
<template>
  <div class="flex gap-2">
    <NuxtLink 
      v-for="link in links" 
      :key="link.text" 
      :to="link.url" 
      class="bg-green-700 hover:bg-green-800 text-white px-4 py-1 rounded-full text-sm transition"
    >
      {{ link.text }}
    </NuxtLink>
  </div>
</template>

<script setup>
const links = [
  { text: 'About Me', url: '/about' },
  { text: 'Impressum', url: '/impressum' },
  { text: 'Projects', url: '#projects' },
  { text: 'Contact', url: '/contact' }
];
</script>