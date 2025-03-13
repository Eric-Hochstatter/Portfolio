<template>
	<section class="text-center mt-12">
		<div class="flex justify-center space-x-4">
			<div
				class="icon-card hover:bg-green-800 hover:shadow-lg transition relative"
			>
				<img
					src="/images/plant.svg"
					alt="Plant"
					class="w-10 h-10 icon"
				/>
				<div
					class="hover-text absolute inset-0 flex items-center justify-center text-white text-center p-2 opacity-0 hover:opacity-100 transition-opacity text-xs"
				>
					Pflanzen
				</div>
			</div>
			<div
				class="icon-card hover:bg-green-800 hover:shadow-lg transition relative"
			>
				<img
					src="/images/camera.svg"
					alt="Camera"
					class="w-10 h-10 icon"
				/>
				<div
					class="hover-text absolute inset-0 flex items-center justify-center text-white text-center p-2 opacity-0 hover:opacity-100 transition-opacity text-xs"
				>
					Fotografie
				</div>
			</div>
			<div
				class="icon-card hover:bg-green-800 hover:shadow-lg transition relative"
			>
				<img
					src="/images/cooking.svg"
					alt="Cooking"
					class="w-10 h-10 icon"
				/>
				<div
					class="hover-text absolute inset-0 flex items-center justify-center text-white text-center p-2 opacity-0 hover:opacity-100 transition-opacity text-xs"
				>
					Kochen
				</div>
			</div>
			<div
				class="icon-card hover:bg-green-800 hover:shadow-lg transition relative"
			>
				<img
					src="/images/travel.svg"
					alt="Travel"
					class="w-10 h-10 icon"
				/>
				<div
					class="hover-text absolute inset-0 flex items-center justify-center text-white text-center p-2 opacity-0 hover:opacity-100 transition-opacity text-xs"
				>
					Reisen
				</div>
			</div>
		</div>
		<p class="mt-4 font-bold">
			Unten gibts einen Einblick in meine Projekte
		</p>
	</section>
</template>

<style scoped>
.icon-card {
	background-color: white;
	box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
	border-radius: 0.5rem;
	padding: 1rem;
	transition: background-color 0.3s, box-shadow 0.3s;
	position: relative;
}

.icon-card:hover {
	background-color: #2f855a; /* Tailwind's green-800 */
	box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1); /* Tailwind's shadow-lg */
}

.icon {
	transition: fill 0.3s;
	fill: currentColor; /* Setzt die Füllfarbe auf die aktuelle Textfarbe */
}

.icon-card:hover .icon {
	fill: white; /* Ändern Sie die Farbe nach Bedarf */
}

.hover-text {
	background-color: #2f855a; /* Hintergrundfarbe für den Text */
	border-radius: 0.5rem;
}
</style>
