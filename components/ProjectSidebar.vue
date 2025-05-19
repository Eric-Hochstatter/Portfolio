// components/ProjectSidebar.vue
<template>
  <aside class="bg-white rounded-lg shadow-sm p-6">
    <!-- Tags -->
    <div class="mb-8">
      <h3 class="text-lg font-bold mb-3 text-green-700">Tags</h3>
      <div class="flex flex-wrap gap-2">
        <span v-for="(tag, index) in tags" :key="index" 
              class="bg-gray-100 px-3 py-1 rounded-full text-sm font-medium">
          {{ tag }}
        </span>
      </div>
    </div>
    
    <!-- Key Learnings -->
    <div v-if="keyLearnings && keyLearnings.length">
      <h3 class="text-lg font-bold mb-3 text-green-700">Key Learnings</h3>
      <ul class="space-y-2">
        <li v-for="(learning, index) in keyLearnings" :key="index" 
            class="flex items-start">
          <svg class="w-5 h-5 mr-2 text-green-700 flex-shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
          </svg>
          <span>{{ learning }}</span>
        </li>
      </ul>
    </div>
    
    <!-- Links/Ressourcen (optional) -->
    <div v-if="links && links.length" class="mt-8">
      <h3 class="text-lg font-bold mb-3 text-green-700">Ressourcen</h3>
      <ul class="space-y-2">
        <li v-for="(link, index) in links" :key="index">
          <a :href="link.url" 
             target="_blank" 
             rel="noopener noreferrer"
             class="text-green-700 hover:text-green-800 flex items-center">
            <svg class="w-4 h-4 mr-2" fill="currentColor" viewBox="0 0 20 20">
              <path d="M11 3a1 1 0 100 2h2.586l-6.293 6.293a1 1 0 101.414 1.414L15 6.414V9a1 1 0 102 0V4a1 1 0 00-1-1h-5z"></path>
              <path d="M5 5a2 2 0 00-2 2v8a2 2 0 002 2h8a2 2 0 002-2v-3a1 1 0 10-2 0v3H5V7h3a1 1 0 000-2H5z"></path>
            </svg>
            {{ link.title }}
          </a>
        </li>
      </ul>
    </div>
  </aside>
</template>

<script setup>
defineProps({
  tags: {
    type: Array,
    default: () => []
  },
  keyLearnings: {
    type: Array,
    default: () => []
  },
  links: {
    type: Array,
    default: () => []
  }
});
</script>