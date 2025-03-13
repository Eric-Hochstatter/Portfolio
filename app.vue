<template>
	<div>
		<!-- <Header /> -->
		<NuxtPage />
		<!-- footer -->
	</div>
</template>

<script setup lang="ts">
useHead({
	title: "Portfolio of Eric Hochstatter",
	meta: [{ name: "description", content: "My amazing site." }],
	htmlAttrs: {
		lang: "en",
	},
	link: [
		{
			rel: "icon",
			type: "image/png",
			href: "/favicon.png",
		},
	],
});

useSeoMeta({
	description: "[description]",
	ogTitle: "Portfolio of Eric Hochstatter",
	ogDescription:
		"Here you can find out more about my design projects, my work process and my skills.",
	ogImage: "/og-image.png",
	ogUrl: "[og:url]",
	twitterTitle: "[twitter:title]",
	twitterDescription: "[twitter:description]",
	twitterImage: "/og-image.png",
	twitterCard: "summary",
});
</script>
