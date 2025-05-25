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
          class="profile-image absolute rounded-full w-20 h-20"
        />
      </span>!
    </h1>

    <div class="flex justify-between items-end mt-40">
      <p class="max-w-2xl text-xl font-medium text-gray-800 text-left leading-relaxed">
        Ich studiere Interaktionsgestaltung an der Hochschule
        für Gestaltung in Schwäbisch Gmünd. Besonders fasziniert
        mich, wie Menschen mit neuen Technologien interagieren –
        und dass ich diese Erlebnisse mitgestalten kann. Mein Fokus
        liegt auf der Entwicklung durchdachter User Experiences.
        Kreatives Tüfteln und das Lösen komplexer Aufgaben sind für
        mich dabei nicht nur Herausforderung, sondern auch Antrieb.
      </p>

      <div class="flex-shrink-0">
        <NuxtLink to="/about" class="learn-more-link inline-flex items-center text-green-700 hover:text-green-800 transition-all">
          Learn more about me!
          <svg class="arrow-icon ml-2 w-6 h-6 transition-all" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M10.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L12.586 11H5a1 1 0 110-2h7.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd"></path>
          </svg>
        </NuxtLink>
      </div>
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

/* Profilbild Animation */
.profile-image {
  display: none;
  position: absolute;
  top: 70px;
  left: 50%;
  transform: translateX(-50%) translateY(-20px);
  border: 2px solid white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  opacity: 0;
  transition: all 0.3s ease-out;
}

/* Hover-Effekt auf "Eric" */
.highlight:hover .profile-image {
  display: block;
  opacity: 1;
  animation: bounceDown 0.8s cubic-bezier(0.68, -0.55, 0.265, 1.55) forwards;
}

/* Bounce-Down Animation */
@keyframes bounceDown {
  0% {
    transform: translateX(-50%) translateY(-20px);
    opacity: 0;
  }
  50% {
    transform: translateX(-50%) translateY(25px);
    opacity: 1;
  }
  65% {
    transform: translateX(-50%) translateY(15px);
  }
  80% {
    transform: translateX(-50%) translateY(22px);
  }
  90% {
    transform: translateX(-50%) translateY(18px);
  }
  100% {
    transform: translateX(-50%) translateY(20px);
    opacity: 1;
  }
}

/* Alternative elegante Swing-Animation (falls du diese bevorzugst) */
@keyframes elegantSwing {
  0% {
    transform: translateX(-50%) translateY(-20px) scale(0.8);
    opacity: 0;
  }
  40% {
    transform: translateX(-50%) translateY(25px) scale(1.05);
    opacity: 1;
  }
  60% {
    transform: translateX(-50%) translateY(15px) scale(0.98);
  }
  80% {
    transform: translateX(-50%) translateY(22px) scale(1.02);
  }
  100% {
    transform: translateX(-50%) translateY(20px) scale(1);
    opacity: 1;
  }
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

/* Learn More Link mit integriertem Pfeil */
.learn-more-link {
  font-size: 1rem;
  transition: font-weight 0.3s;
  display: inline-flex;
  align-items: center;
}

.learn-more-link:hover {
  font-weight: 500;
}

/* Pfeil innerhalb des Links */
.learn-more-link .arrow-icon {
  transition: transform 0.3s ease;
  flex-shrink: 0; /* Verhindert Größenänderung des SVGs */
}

.learn-more-link:hover .arrow-icon {
  transform: rotate(45deg);
}
</style>