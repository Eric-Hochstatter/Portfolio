<template>
  <div class="bg-beige min-h-screen">
    <!-- Navigation -->
    <div class="max-w-6xl mx-auto px-6 py-8">
      <div class="flex justify-between items-center">
        <NuxtLink to="/" class="text-green-700 hover:text-green-800 flex items-center">
          <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 19l-7-7m0 0l7-7m-7 7h18"></path>
          </svg>
          Zurück zur Übersicht
        </NuxtLink>
        <NavButtons />
      </div>
    </div>

    <!-- Project Header -->
    <div class="max-w-6xl mx-auto px-6 mt-8">
      <div class="bg-white rounded-lg shadow-sm p-12">
        <div class="flex flex-col md:flex-row justify-between">
          <div>
            <h1 class="text-4xl font-bold mb-2">{{ title }}</h1>
            <p class="text-xl mb-6">{{ subtitle }}</p>

            <div class="prose max-w-xl">
              <p>{{ description }}</p>
            </div>
          </div>
          
          <div class="mt-8 md:mt-0">
            <div class="bg-gray-50 p-6 rounded-lg">
              <h3 class="font-medium text-gray-700 mb-2">Projektdauer</h3>
              <p class="text-sm mb-4">{{ timeline }}</p>
              
              <h3 class="font-medium text-gray-700 mb-2">Team</h3>
              <p class="text-sm mb-4">
                <span v-for="(member, index) in team" :key="index">
                  {{ member }}<br v-if="index < team.length - 1">
                </span>
              </p>
              
              <h3 class="font-medium text-gray-700 mb-2">Tools</h3>
              <p class="text-sm">
                <span v-for="(tool, index) in tools" :key="index">
                  {{ tool }}<br v-if="index < tools.length - 1">
                </span>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Main Content -->
    <div class="max-w-6xl mx-auto px-6 mt-12">
      <!-- Slot für projektspezifischen Inhalt -->
      <slot></slot>

      <!-- Next Project Section -->
      <div class="bg-white rounded-lg shadow-sm p-12 mt-12">
        <div class="flex justify-between items-center">
          <div>
            <h3 class="text-xl font-medium">Nächstes Projekt</h3>
            <h2 class="text-3xl font-bold text-green-700">{{ nextProjectTitle }}</h2>
          </div>
          <NuxtLink :to="nextProjectPath" class="bg-green-700 hover:bg-green-800 text-white px-6 py-3 rounded-full transition flex items-center">
            Ansehen
            <svg class="ml-2 w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
            </svg>
          </NuxtLink>
        </div>
      </div>
    </div>

    <!-- Footer -->
    <div class="max-w-6xl mx-auto px-6 mt-12 pb-12">
      <div class="border-t border-gray-200 pt-8 text-center">
        <p class="text-sm text-gray-500">Design & Development by Eric Hochstatter © 2025</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import NavButtons from '~/components/NavButtons.vue';

const props = defineProps({
  title: String,
  subtitle: String,
  description: String,
  timeline: String,
  team: Array,
  tools: Array,
  nextProjectTitle: String,
  nextProjectPath: String
});
</script>

<style scoped>
.bg-beige {
  background-color: #f8f8f1;
}

.prose p {
  margin-bottom: 1rem;
  line-height: 1.7;
}
</style>