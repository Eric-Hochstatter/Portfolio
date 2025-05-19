// components/ProjectNextSection.vue
<template>
  <section class="mt-20">
    <h2 class="text-2xl font-bold mb-8 text-green-700">{{ title }}</h2>
    
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <div v-for="(project, index) in projects" :key="index" class="overflow-hidden rounded-lg shadow-sm relative group h-64">
        <!-- Bild -->
        <img :src="project.image" :alt="project.title" class="w-full h-full object-cover transition-transform duration-500 scale-110 group-hover:scale-120" />
        
        <!-- Dunkler Verlauf Overlay (nur sichtbar bei Hover) -->
        <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-black/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
        
        <!-- Inhalt (Titel, Untertitel) -->
        <div class="absolute bottom-0 left-0 p-4 text-white z-10">
          <!-- Titel und Untertitel mit Opacity-Transition -->
          <div class="opacity-0 group-hover:opacity-100 transition-opacity duration-500">
            <h3 class="text-xl font-bold">{{ project.title }}</h3>
            <p class="text-sm font-medium opacity-90">{{ project.subtitle }}</p>
          </div>
        </div>
        
        <!-- Klickbarer Link über das gesamte Element -->
        <NuxtLink :to="project.url" class="absolute inset-0 z-20"></NuxtLink>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    default: 'Weitere Projekte'
  },
  projects: {
    type: Array,
    default: () => [],
    // Erwartetes Format: [{ title: '', subtitle: '', image: '', url: '' }, ...]
  }
});
</script>

<style scoped>
/* Hover-Effekt für die Projektkarten (ähnlich wie in ProjectCard.vue) */
.group:hover img {
  transform: scale(1.1);
}
</style>