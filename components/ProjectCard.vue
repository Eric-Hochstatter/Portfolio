<template>
	<div>
		<NuxtLink :to="url">
			<div
				class="bg-gray-600 text-white shadow-none hover:bg-red400 shadow-gray-500 hover:shadow-110 hover:z-10 transition-shadow duration-200"
			>
				<img :src="image" alt="image" />
				<h3>{{ title }}</h3>
				<h4>{{ subtitle }}</h4>
			</div>
		</NuxtLink>
	</div>
</template>

<script lang="ts" setup>
defineProps({
	// title: {
	// 	type: String,
	// 	default: "Title",
	// },
	title: String,
	subtitle: String,
	image: String,
	url: String,
});
</script>

<style></style>
