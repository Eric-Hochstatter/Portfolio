<template>
	<section class="mt-12">
		<h2 class="text-2xl font-bold text-center mb-6">Recent Projects</h2>

		<div
			class="grid grid-cols-1 md:grid-cols-2 w-full md:w-4/5 lg:w-1/2 mx-auto gap-6"
		>
			<ProjectCard
				image="/images/travello-titelbild.jpg"
				title="Travello"
				description="Konzipierung einer App"
				:tags="['UX-Research', 'Prototyping', 'App-Entwicklung']"
				class="col-span-1 md:col-span-2"
			/>

			<ProjectCard
				image="/images/Focal-titelbild.jpg"
				title="Focal"
				description="Ein Konzept zum räumlichen Arbeiten"
				:tags="['Interaction Design', 'Gesture control', 'VR/MR']"
			/>

			<ProjectCard
				image="/images/CelestialBodies-titelbild.jpg"
				title="Celestial Bodies"
				description="Entwicklung einer interaktiven Ausstellung"
				:tags="['Arduino', 'Interaction', 'Exhibition']"
			/>
		</div>
	</section>
</template>

<script setup>
import ProjectCard from "./ProjectCard.vue";
</script>
