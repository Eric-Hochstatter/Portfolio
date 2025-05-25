// pages/projects/celestial-bodies.vue
<template>
  <div class="bg-beige min-h-screen pb-24">
    <!-- Zurück-Navigation -->
    <div class="max-w-6xl mx-auto px-6 pt-12">
      <NuxtLink to="/" class="back-link flex items-center text-green-700 hover:text-green-800 transition-all">
        <svg class="mr-2 w-5 h-5 transition-all" fill="currentColor" viewBox="0 0 20 20">
          <path fill-rule="evenodd" d="M9.707 14.707a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 1.414L7.414 9H15a1 1 0 110 2H7.414l2.293 2.293a1 1 0 010 1.414z" clip-rule="evenodd"></path>
        </svg>
        Zurück zur Übersicht
      </NuxtLink>
    </div>

    <!-- Hauptinhalt basierend auf dem Screenshot -->
    <div class="max-w-6xl mx-auto px-6">
      <!-- Header-Bereich: zwei separate Kacheln nebeneinander -->
      <div class="grid grid-cols-1 md:grid-cols-12 gap-6 mt-8">
        <!-- Linke Kachel: Projekttitel und Beschreibung -->
        <div class="md:col-span-8 bg-white rounded-lg shadow-sm p-12 flex flex-col h-full">
          <div>
            <h1 class="text-5xl font-bold mb-2">Celestial Bodies</h1>
            <p class="text-2xl mb-12">Interaktives Ausstellungskonzept</p>
          </div>
          
          <div class="mt-auto">
            <p class="text-base">
                Das Projekt für unseren Kurs „Interaktive Kommunikationssysteme“ stellte uns vor die Aufgabe, eine einfache Buchseite aus einem Kinderlexikon in eine dynamische, fesselnde Ausstellung zu verwandeln. Unser Thema, „Asteroiden, Kometen und Meteoriten“, taucht ein in die faszinierende Welt dieser Himmelskörper und beleuchtet ihre Ursprünge, Eigenschaften und ihre Bedeutung innerhalb unseres Sonnensystems. Unser Ziel war es, ein immersives Bildungserlebnis zu schaffen, das Besucher jeden Alters begeistert.            </p>
          </div>
        </div>
        
        <!-- Rechte Kachel: Projektinfos -->
        <div class="md:col-span-4 bg-white rounded-lg shadow-sm p-12 flex flex-col h-full">
          <div class="space-y-8">
            <!-- Projektdauer -->
            <div>
              <h3 class="text-lg font-semibold mb-2">Projektdauer</h3>
              <p>
                Februar '24 -<br>
                Juli '24
              </p>
            </div>
            
            <!-- Team -->
            <div>
              <h3 class="text-lg font-semibold mb-2">Team</h3>
              <p>
                <a href="https://brunogross.com/" target="_blank" rel="noopener noreferrer" class="team-link">Bruno Gross</a>,<br>
                <a href="https://yasminhaehnel.com/" target="_blank" rel="noopener noreferrer" class="team-link">Yasmin Hähnel</a>
              </p>
            </div>
            
            <!-- Tools -->
            <div>
              <h3 class="text-lg font-semibold mb-2">Tools</h3>
              <p>
                After Effects,<br>
                Arduino,<br>
                Figma,<br>
                Fusion 360
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Wireframes-Bereich ohne Kachel, direkt auf Hintergrund -->
      <div class="mt-16 mb-16">
        <img 
          src="/images/projects/CelestialBodies/SkizzenCelestialBodies.png" 
          alt="Celestial Bodies Wireframes" 
          class="w-full max-w-6xl mx-auto" 
          onerror="this.src='/images/placeholder.jpg'" 
        />
      </div>

      <!-- Video-Bereich mit Click-to-Play -->
      <div class="mt-8">
        <div class="video-container relative overflow-hidden rounded-lg bg-white">
          <!-- Vorschaubild (wird beim Klick ausgeblendet) -->
          <img 
            v-show="!videoPlaying"
            src="/images/projects/CelestialBodies/Foto-Wandmodell.jpg" 
            alt="Celestial Bodies Demo" 
            class="w-full h-full object-cover cursor-pointer transition-opacity duration-500" 
            @click="startVideo"
          />
          
          <!-- Play-Button Icon (nur sichtbar, wenn Video nicht spielt) -->
          <div 
            v-show="!videoPlaying"
            class="absolute inset-0 flex items-center justify-center cursor-pointer z-10"
            @click="startVideo"
          >
            <div class="bg-black bg-opacity-50 p-4 rounded-full hover:bg-opacity-70 transition-all duration-300">
              <svg class="w-12 h-12 text-white" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd"></path>
              </svg>
            </div>
          </div>
          
          <!-- MP4 Video (wird beim Klick sichtbar) -->
          <video 
            v-show="videoPlaying"
            ref="videoElement"
            class="w-full h-full object-cover"
            controls
            autoplay
            loop
            muted
          >
            <source src="/videos/celestial-bodies-demo.mp4" type="video/mp4">
            Dein Browser unterstützt das Video-Element nicht.
          </video>
        </div>
      </div>

      <!-- Projektbeschreibung -->
      <div class="mt-8 bg-white rounded-lg shadow-sm p-12">
        <h2 class="text-2xl font-bold mb-6">Entdecke das Weltall interaktiv!</h2>
        <p class="mb-4">
          Celestial Bodies bringt die Wunder des Universums in greifbare Nähe. Durch Arduino-gesteuerte Installationen können Besucher Planeten erforschen, Sterne zum Leuchten bringen und die Geheimnisse des Kosmos auf eine völlig neue Art erleben. Das interaktive Ausstellungskonzept verbindet Wissenschaft mit Technologie und schafft unvergessliche Erlebnisse für Jung und Alt.
        </p>
      </div>

      <!-- App Screenshots im Layout wie in ProjectsGrid -->
      <div class="mt-12 max-w-6xl mx-auto">
        <!-- Grid ähnlich wie in ProjectsGrid.vue -->
        <div class="grid grid-cols-1 md:grid-cols-6 gap-6" style="grid-template-rows: auto auto;">
          <!-- Obere Reihe: Hauptinstallation (breiter) und Detail -->
          <div class="md:col-span-2 md:row-span-2 bg-white rounded-lg overflow-hidden">
            <img src="/images/projects/CelestialBodies/SchaudieWandan.png" alt="Celestial Bodies Hauptinstallation" class="w-full h-full object-cover" onerror="this.src='/images/placeholder.jpg'" />
          </div>
          
          <!-- Rechte Seite: Detail über 2 Reihen -->
          <div class="md:col-span-2 bg-white rounded-lg overflow-hidden">
            <img src="/images/projects/CelestialBodies/IMG_5262.JPG" alt="Celestial Bodies Detail" class="w-full h-full object-cover" onerror="this.src='/images/placeholder.jpg'" />
          </div>
          
         
          <div class="md:col-span-2 bg-white rounded-lg overflow-hidden aspect-square">
            <img src="/images/projects/CelestialBodies/Asteroiden.jpeg" alt="Celestial Bodies Interaktion" class="w-full h-full object-cover" onerror="this.src='/images/placeholder.jpg'" />
          </div>
          
          <div class="md:col-span-4 md:row-span-1 bg-white rounded-lg overflow-hidden">
            <img src="/images/projects/CelestialBodies/Terminal.png" alt="Celestial Bodies Übersicht" class="w-full h-full object-cover" onerror="this.src='/images/placeholder.jpg'" />
          </div>
        </div>
      </div>

      <!-- Erlerntes -->
      <div class="mt-12 bg-white rounded-lg shadow-sm p-12">
        <h2 class="text-2xl font-bold mb-6">Erlerntes & genutztes</h2>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
          <div>
            <h3 class="font-bold mb-2">Arduino Programmierung</h3>
            <p class="text-sm">Vertiefte Kenntnisse in der Entwicklung interaktiver Hardware-Installationen mit Sensoren und Aktoren.</p>
          </div>
          <div>
            <h3 class="font-bold mb-2">Prototyping & Fabrication</h3>
            <p class="text-sm">Von der digitalen Planung in Fusion 360 bis zur physischen Umsetzung komplexer interaktiver Objekte.</p>
          </div>
          <div>
            <h3 class="font-bold mb-2">Experience Design</h3>
            <p class="text-sm">Gestaltung immersiver Erlebnisse, die Besucher emotional ansprechen und zum Entdecken einladen.</p>
          </div>
        </div>
      </div>

      <!-- Nächstes Projekt -->
      <div class="mt-12 bg-white rounded-lg shadow-sm p-12 pb-16 relative">
        <div class="flex justify-between items-end">
          <div>
            <h2 class="text-5xl font-bold text-black">Nächstes Projekt</h2>
            <h3 class="text-2xl font-bold text-green-700 mt-16">Focal</h3>
            <p class="text-lg text-black mt-2">Konzept für räumliches arbeiten</p>
          </div>
          <NuxtLink to="/projects/focal" class="project-arrow-link text-white w-12 h-12 rounded-full transition flex items-center justify-center">
            <svg class="arrow-icon w-6 h-6 transition-all duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
            </svg>
          </NuxtLink>
        </div>

        <!-- Trennstrich und "Designed by"-Hinweis -->
        <div class="footer-divider">
          <div class="divider"></div>
          <p class="designed-by">Designed & Coded 2025 by © Eric Hochstatter</p>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
// Reactive state für Video-Wiedergabe
const videoPlaying = ref(false);
const videoElement = ref(null);

// Funktion zum Starten des Videos
const startVideo = () => {
  videoPlaying.value = true;
  // Optional: Video nach dem Einblenden starten
  nextTick(() => {
    if (videoElement.value) {
      videoElement.value.play().catch(console.error);
    }
  });
};
</script>

<style scoped>
.bg-beige {
  background-color: #F2F2F2;
}

.back-link {
  display: inline-flex;
  align-items: center;
  font-weight: 500;
  transition: all 0.3s;
}

.back-link:hover svg {
  transform: translateX(-4px);
}

.team-link {
  color: #2f855a; /* Grüne Farbe, passend zum Rest deiner Seite */
  transition: color 0.3s;
  text-decoration: none;
}

/* Styling für den Video-Container */
.video-container {
  height: 0;
  padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
  position: relative;
}

.video-container img,
.video-container iframe,
.video-container video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Footer-Divider Styles */
.footer-divider {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 0.75rem;
  text-align: center;
}

.divider {
  height: 1px;
  background-color: #e2e8f0;
  margin-bottom: 0.75rem;
  margin-left: 32px;
  margin-right: 32px;
}

.designed-by {
  font-size: 0.75rem;
  color: #94a3b8;
  font-weight: 400;
}

/* Hover-Effekt für den Projekt-Pfeil */
.project-arrow-link {
  background-color: black;
  transition: all 0.3s ease;
}

.project-arrow-link:hover {
  background-color: #2f855a;
}

.project-arrow-link .arrow-icon {
  transition: transform 0.3s ease;
}

.project-arrow-link:hover .arrow-icon {
  transform: rotate(-45deg);
}
</style>