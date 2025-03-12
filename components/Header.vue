<template>
	<div>
		<NuxtLink to="/">Home</NuxtLink> |
		<NuxtLink to="/about">About</NuxtLink>
	</div>
</template>

<script lang="ts" setup></script>

<style>
.router-link-exact-active {
	text-decoration: underline;
	font-weight: bold;
}
</style>
