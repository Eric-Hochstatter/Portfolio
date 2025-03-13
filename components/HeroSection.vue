<template>
	<section class="text-center p-12">
		<h1 class="text-4xl font-bold">
			Hey, ich bin
			<span class="highlight relative"
				>Eric
				<img
					src="/images/its-me.jpeg"
					alt="Eric"
					class="hidden absolute rounded-full w-18 h-18"
				/> </span
			>!
		</h1>
		<p class="max-w-2xl mx-auto mt-12 text-lg text-gray-700 text-left">
			Ich studiere Interaktionsgestaltung (B.A.) an der Hochschule für
			Gestaltung in Schwäbisch Gmünd. Die Interaktion zwischen Menschen
			und neuen Technologien fasziniert mich – besonders, weil ich sie an
			vorderster Front miterleben und mitgestalten kann. Dabei liegt mein
			Fokus darauf, eine stimmige User Experience zu schaffen. Das Tüfteln
			an neuen Ideen und die Suche nach kreativen Lösungen für komplexe
			Probleme helfen mir, meinen Horizont als Gestalter stetig zu
			erweitern. Ich liebe es, dabei neue Dinge zu lernen, die mich in
			meiner Arbeit weiterbringen.
		</p>
	</section>
</template>

<style scoped>
.highlight {
	color: #2f855a; /* Tailwind's green-800 */
	position: relative;
}

.highlight:hover img {
	display: block;
}

.highlight img {
	display: none;
	position: absolute;
	top: -80px; /* Adjust as needed */
	left: 50%;
	transform: translateX(-50%);
	border: 2px solid white;
	box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>
