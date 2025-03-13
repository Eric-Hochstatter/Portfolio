<template>
	<div
		class="relative group overflow-hidden rounded-lg shadow-lg cursor-pointer"
	>
		<!-- Image mit Zoom-Effekt -->
		<img
			:src="image"
			:alt="title"
			class="w-full h-auto object-cover transition-transform duration-500 group-hover:scale-110"
		/>

		<!-- Overlay -->
		<div
			class="absolute inset-0 bg-opacity-50 group-hover:bg-opacity-70 transition-opacity duration-500 flex flex-col justify-end p-4"
		>
			<h3 class="text-white font-bold text-lg">{{ title }}</h3>
			<p class="text-gray-300 text-sm">{{ description }}</p>

			<!-- Tags (nur sichtbar bei Hover) -->
			<div
				class="flex gap-2 mt-2 opacity-0 group-hover:opacity-100 transition-opacity duration-500"
			>
				<span
					v-for="tag in tags"
					:key="tag"
					class="bg-gray-800 text-white text-xs px-2 py-1 rounded-full"
				>
					{{ tag }}
				</span>
			</div>
		</div>
	</div>
</template>

<script setup>
defineProps({
	image: String,
	title: String,
	description: String,
	tags: Array,
});
</script>
