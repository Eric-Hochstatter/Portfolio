// components/ProjectCard.vue
<template>
  <div class="relative overflow-hidden group" :class="cardHeight">
    <!-- Bild -->
    <img 
      :src="image" 
      :alt="title" 
      class="w-full h-full object-cover transition-transform duration-500 scale-110 group-hover:scale-120"
    />
    
    <!-- Dunkler Verlauf Overlay (nur sichtbar bei Hover) -->
    <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-black/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
    
    <!-- Inhalt (Titel, Untertitel, Tags) -->
    <div class="absolute bottom-0 left-0 p-4 text-white z-10">
      <!-- Titel und Untertitel mit Opacity-Transition -->
      <div class="opacity-0 group-hover:opacity-100 transition-opacity duration-500">
        <h3 class="text-2xl font-bold">{{ title }}</h3>
        <p class="text-m font-medium opacity-90">{{ subtitle }}</p>
      </div>
      
      <!-- Tags -->
      <div
        class="flex gap-2 mt-2 opacity-0 group-hover:opacity-100 transition-opacity duration-500"
      >
        <span
          v-for="tag in tags"
          :key="tag"
          class="bg-black text-white text-xs px-2 py-1 rounded-full"
        >
          {{ tag }}
        </span>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  title: String,
  subtitle: String,
  image: String,
  tags: Array,
  fullWidth: {
    type: Boolean,
    default: false
  }
});

const cardHeight = computed(() => {
  return props.fullWidth ? 'h-80' : 'h-64';
});
</script>

<style scoped>
.relative {
  width: 100%;
  height: 100%; /* Ensure the container takes the full height */
  border-radius: 0.5rem; /* Entspricht Tailwind's rounded-lg */
}

img {
  display: block; /* Remove any default spacing around the image */
  border-radius: 0.5rem; /* Rundet auch das Bild ab */
}
</style>