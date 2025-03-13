<template>
	<div class="bg-beige min-h-screen p-8">
		<!-- Navigation (fix oben) -->
		<Navigation />

		<!-- GRID LAYOUT -->
		<div class="grid grid-cols-10 gap-x-4">
			<!-- HERO SECTION: Nimmt die vollen 10 Spalten ein -->
			<div class="col-span-10 text-center">
				<HeroSection />
			</div>

			<!-- ABOUT SECTION: Nimmt 6 von 10 Spalten -->
			<div class="col-span-6">
				<AboutSection />
			</div>

			<!-- Floating Menu: Fixiert rechts -->
			<div class="fixed right-5 top-1/2 transform -translate-y-1/2">
				<FloatingMenu @scrollToProjects="scrollToProjects" />
			</div>

			<!-- PROJECT PREVIEW: Nimmt alle 10 Spalten ein -->
			<div class="col-span-10">
				<HobbyCard />
			</div>

			<!-- PROJECTS Section (Hier soll hingesprungen werden) -->
			<div ref="projectsSection" class="col-span-10 mt-20">
				<ProjectPreview />
			</div>
		</div>
	</div>
</template>

<script setup>
import Navigation from "@/components/Navigation.vue";
import HeroSection from "@/components/HeroSection.vue";
import AboutSection from "@/components/AboutSection.vue";
import HobbyCard from "@/components/HobbyCard.vue";
import ProjectPreview from "@/components/ProjectPreview.vue";
import FloatingMenu from "@/components/FloatingMenu.vue";
import { ref } from "vue";

// Reference für den Scrollbereich
const projectsSection = ref(null);

const scrollToProjects = () => {
	if (projectsSection.value) {
		projectsSection.value.scrollIntoView({ behavior: "smooth" });
	} else {
		console.error("projectsSection reference is not set!");
	}
};
</script>

<style scoped>
.bg-beige {
	background-color: #f5f2e9;
}
</style>
