// components/ProjectHeader.vue
<template>
  <div class="max-w-6xl mx-auto px-6 mt-8">
    <!-- Projekttitel und Metadaten -->
    <div class="flex flex-col md:flex-row justify-between mb-8">
      <div>
        <h1 class="text-4xl md:text-5xl font-bold mb-2">{{ title }}</h1>
        <p class="text-xl text-gray-700 mb-4">{{ subtitle }}</p>
      </div>
      <div class="mt-4 md:mt-0">
        <div class="flex flex-col space-y-6">
          <!-- Projektdauer -->
          <div>
            <h3 class="text-sm font-semibold text-gray-500 mb-1">Projektdauer</h3>
            <p class="font-medium">{{ period }}</p>
          </div>
          
          <!-- Team -->
          <div v-if="team && team.length">
            <h3 class="text-sm font-semibold text-gray-500 mb-1">Team</h3>
            <ul>
              <li v-for="(member, index) in team" :key="index" class="font-medium">
                {{ member }}
              </li>
            </ul>
          </div>
          
          <!-- Tools -->
          <div v-if="tools && tools.length">
            <h3 class="text-sm font-semibold text-gray-500 mb-1">Tools</h3>
            <ul class="flex flex-wrap gap-2">
              <li v-for="(tool, index) in tools" :key="index" 
                  class="inline-block bg-gray-100 px-3 py-1 rounded-full text-sm font-medium">
                {{ tool }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Hero-Bild -->
    <div class="w-full h-[500px] rounded-lg overflow-hidden">
      <img :src="imageSrc" :alt="title" class="w-full h-full object-cover" />
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  subtitle: {
    type: String,
    default: ''
  },
  period: {
    type: String,
    default: ''
  },
  team: {
    type: Array,
    default: () => []
  },
  tools: {
    type: Array,
    default: () => []
  },
  imageSrc: {
    type: String,
    required: true
  }
});
</script>