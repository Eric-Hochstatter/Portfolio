<template>
	<div
		class="fixed right-5 top-1/2 transform -translate-y-1/2 flex flex-col space-y-2"
	>
		<!-- Erster Button (Scroll zum oberen Rand der Seite) -->
		<button class="floating-btn" @click="scrollToTop">
			<img src="/images/User.svg" alt="User Icon" class="w-6 h-6" />
		</button>

		<!-- Zweiter Button (Scroll zu Projekten) -->
		<button class="floating-btn" @click="handleScrollToProjects">
			<img src="/images/Projects.svg" alt="Grid Icon" class="w-6 h-6" />
		</button>
	</div>
</template>

<script setup>
const emit = defineEmits(["scrollToProjects"]);

const scrollToTop = () => {
	window.scrollTo({ top: 0, behavior: "smooth" });
};

const handleScrollToProjects = () => {
	emit("scrollToProjects");
};
</script>

<style scoped>
.floating-btn {
	background-color: white; /* bg-green-700 */
	color: white; /* text-white */
	border-radius: 9999px; /* rounded-full */
	width: 3rem; /* w-12 */
	height: 3rem; /* h-12 */
	display: flex; /* flex */
	align-items: center; /* items-center */
	justify-content: center; /* justify-center */
	transition: background-color 0.2s; /* transition */
}
.floating-btn:hover {
	background-color: #065f46; /* hover:bg-green-800 */
}
</style>
