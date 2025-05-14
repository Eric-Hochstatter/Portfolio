<template>
  <section class="relative bg-white rounded-lg shadow-sm p-12 mx-auto max-w-9xl">
    <!-- Navigation oben rechts -->
    <div class="absolute top-12 right-12">
      <nav class="flex justify-end space-x-4">
        <NuxtLink to="/about" class="btn">About Me</NuxtLink>
        <NuxtLink to="#projects" class="btn">Projects</NuxtLink>
        <NuxtLink to="#" class="btn">Playground</NuxtLink>
        <NuxtLink to="#" class="btn">Contact</NuxtLink>
      </nav>
    </div>

    <!-- Hero Content -->
    <h1 class="text-5xl font-bold mb-12">
      Hi, it's <span class="highlight relative">Eric
        <img
          src="/images/its-me.jpeg"
          alt="Eric"
          class="hidden absolute rounded-full w-20 h-20"
        />
      </span>!
    </h1>

    <p class="max-w-2xl text-xl font-medium text-gray-800 text-left leading-relaxed mt-32">
      Ich studiere Interaktionsgestaltung an der Hochschule
      für Gestaltung in Schwäbisch Gmünd. Besonders fasziniert
      mich, wie Menschen mit neuen Technologien interagieren –
      und dass ich diese Erlebnisse mitgestalten kann. Mein Fokus
      liegt auf der Entwicklung durchdachter User Experiences.
      Kreatives Tüfteln und das Lösen komplexer Aufgaben sind für
      mich dabei nicht nur Herausforderung, sondern auch Antrieb.
    </p>

    <div class="mt-12 text-right">
      <NuxtLink to="/about" class="learn-more-link inline-flex items-center text-green-700 hover:text-green-800 transition-all">
        Learn more about me!
        <svg class="ml-2 w-6 h-6 transition-all" fill="currentColor" viewBox="0 0 20 20">
          <path fill-rule="evenodd" d="M10.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L12.586 11H5a1 1 0 110-2h7.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd"></path>
        </svg>
      </NuxtLink>
    </div>
  </section>
</template>

<script setup>
// Du musst NuxtLink importieren, wenn es nicht automatisch verfügbar ist
// import { NuxtLink } from '#components';
</script>

<style scoped>
.highlight {
  color: #2f855a; /* Tailwind's green-800 */
  position: relative;
  text-decoration: underline;
  text-decoration-color: #2f855a;
  text-underline-offset: 4px;
}

.highlight:hover img {
  display: block;
}

.highlight img {
  display: none;
  position: absolute;
  top: 70px;
  left: 50%;
  transform: translateX(-50%);
  border: 2px solid white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

/* Knopfstil aus der Navigation.vue */
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

/* Learn More Link Hover-Effekt */
.learn-more-link {
  font-size: 1rem;
  transition: font-size 0.3s, transform 0.3s;
}

.learn-more-link:hover {
  font-size: 1rem;
  font-weight: 500;
}

.learn-more-link:hover svg {
  width: 1.75rem;
  height: 1.75rem;
  rotate: 45deg;
}
</style>
