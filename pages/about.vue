// pages/index.vue
<template>
  <div class="bg-beige min-h-screen pb-24">
    <!-- Top Navigation -->
    <div class="flex justify-end p-4">

    </div>
    
    <!-- Hero Section -->
    <div class="max-w-6xl mx-auto px-6 mt-12 mb-12">
      <HeroSection />
    </div>
    
    <!-- Projects Grid -->
    <div class="max-w-6xl mx-auto mt-12">
      <ProjectsGrid />
    </div>
    
    <!-- Internship Notice -->
    <div class="max-w-6xl mx-auto px-6 mt-12">
      <InternshipNotice />
    </div>
  </div>
</template>

<script setup>
import HeroSection from '~/components/HeroSection.vue';
import ProjectsGrid from '~/components/ProjectsGrid.vue';
import InternshipNotice from '~/components/InternshipNotice.vue';
import FloatingMenu from "@/components/FloatingMenu.vue";
</script>

<style scoped>
.bg-beige {
	background-color: #f8f8f1;
}
</style>