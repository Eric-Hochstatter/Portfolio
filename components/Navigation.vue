<template>
	<nav class="flex justify-end space-x-4 p-4">
		<NuxtLink to="/about" class="btn">About Me</NuxtLink>
		<NuxtLink to="#" class="btn">Projects</NuxtLink>
		<NuxtLink to="#" class="btn">Playground</NuxtLink>
		<NuxtLink to="#" class="btn">Contact</NuxtLink>
	</nav>
</template>

<style scoped>
.btn {
	background-color: #2f855a;
	color: white;
	padding-left: 1rem;
	padding-right: 1rem;
	padding-top: 0.5rem;
	padding-bottom: 0.5rem;
	border-radius: 2rem;
	transition: background-color 0.3s;
}
.btn:hover {
	background-color: #1c5337;
}
</style>
