<template>
  <div id="projects" class="max-w-6xl mx-auto px-6">
    <div 
      class="grid grid-cols-1 md:grid-cols-6 gap-6"
      style="grid-template-rows: 352px 352px;"
    >

      <!-- Travello -->
      <div class="md:col-span-4 md:row-span-1">
        <ProjectCard
          image="/images/projects/travello-titelbild.jpg"
          title="travello"
          subtitle="Konzeptentwicklung einer App"
          :tags="['UX-Research', 'Prototyping', 'App-Entwicklung']"
        />
      </div>

      <!-- Celestial Bodies: rechts über 2 Reihen -->
      <div class="md:col-span-2 md:row-span-2">
        <ProjectCard
          title="Celestial Bodies"
          subtitle="Interaktives Ausstellungskonzept"
          image="/images/projects/CelestialBodies-titelbild.jpg"
          :tags="['Arduino', 'Interaction', 'Exhibition']"
        />
      </div>

      <!-- Focal -->
      <div class="md:col-span-2 aspect-square">
        <ProjectCard
          title="Focal"
          subtitle="Konzept für räumliches arbeiten"
          image="/images/projects/Focal-titelbild.jpg"
          :tags="['Interaction Design', 'Gesture control', 'VR/MR']"
        />
      </div>

      <!-- comigo -->
      <div class="md:col-span-2 aspect-square">
        <ProjectCard
          title="comigo"
          subtitle="Design-Sprint"
          image="/images/projects/comigo-titelbild.jpg"
          :tags="['Design Sprint', 'App-Entwicklung', 'UX-Research']"
        />
      </div>

    </div>
  </div>
</template>

<script setup>
import ProjectCard from './ProjectCard.vue';
</script>
