// components/ProjectGallery.vue
<template>
  <section class="my-16">
    <h2 class="text-2xl font-bold mb-6 text-green-700">Galerie</h2>
    
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div v-for="(image, index) in images" :key="index" class="overflow-hidden rounded-lg shadow-sm group">
        <div class="relative">
          <!-- Bild -->
          <img :src="image.src" :alt="image.alt" class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-105" />
          
          <!-- Caption (Overlay unten) -->
          <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-60 text-white p-3 transform translate-y-full group-hover:translate-y-0 transition-transform duration-300">
            <p>{{ image.caption }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  images: {
    type: Array,
    default: () => [],
    // Erwartetes Format: [{ src: '', alt: '', caption: '' }, ...]
  }
});
</script>