// pages/projects/travello.vue
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
            <h1 class="text-5xl font-bold mb-2">travello</h1>
            <p class="text-2xl mb-12">Die smarte Art, gemeinsam zu reisen!</p>
          </div>
          
          <div class="mt-auto"> <!-- Margin-bottom entfernt, damit Text genau unten abschließt -->
            <p class="text-base">
              Mit travello wird die Reiseplanung in der Gruppe einfacher gestaltet. Keine endlosen Chats, keine Missverständnisse – stattdessen werden eure Wünsche gebündelt. Inspiration entdecken, Ideen sammeln, abstimmen und automatisch einen individuellen Tagesplan erhalten. Verschafft euch mit travello einen klaren Überblick über die besten Spots und gestaltet eine Planung, die wirklich zu euch passt!
            </p>
          </div>
        </div>
        
        <!-- Rechte Kachel: Projektinfos -->
        <div class="md:col-span-4 bg-white rounded-lg shadow-sm p-12 flex flex-col h-full">
          <div class="space-y-8">
            <!-- Projektdauer -->
            <div>
              <h3 class="text-lg font-semibold mb-2">Projektdauer</h3>
              <p>
                Oktober '24 -<br>
                Februar '25
              </p>
            </div>
            
            <!-- Team -->
           <div>
  <h3 class="text-lg font-semibold mb-2">Team</h3>
  <p>
    <a href="https://leaullmann.de/" target="_blank" rel="noopener noreferrer" class="team-link">Lea Ullmann</a>,<br>
    <a href="https://yasminhaehnel.com/" target="_blank" rel="noopener noreferrer" class="team-link">Yasmin Hähnel</a>
  </p>
</div>
            
            <!-- Tools -->
            <div>
              <h3 class="text-lg font-semibold mb-2">Tools</h3>
              <p>
                Figma,<br>
                Miro,<br>
                Notion
              </p>
            </div>
          </div>
        </div>
      </div>

      

        <!-- Wireframes-Bereich ohne Kachel, direkt auf Hintergrund -->
      <div class="mt-16 mb-16">
        <img 
          src="/images/projects/travello/Travello-Skizzen.png" 
          alt="travello Wireframes" 
          class="w-full max-w-6xl mx-auto" 
          onerror="this.src='/images/placeholder.jpg'" 
        />
      </div>

      <!-- Video-Bereich mit Click-to-Play (ersetzt das Hauptbild) -->
      <div class="mt-8">
        <div class="video-container relative overflow-hidden rounded-lg bg-white">
          <!-- Vorschaubild (wird beim Klick ausgeblendet) -->
          <img 
            v-show="!videoPlaying"
            src="/images/projects/travello-titelbild.jpg" 
            alt="travello App Screenshot" 
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
          
          <!-- YouTube Video (wird beim Klick sichtbar) -->
          <div v-show="videoPlaying" class="w-full">
            <iframe 
              width="100%" 
              height="100%" 
              :src="videoSrc" 
              title="travello App Demo" 
              frameborder="0" 
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
              allowfullscreen
              class="w-full aspect-video"
            ></iframe>
          </div>
        </div>
      </div>

      <!-- Projektbeschreibung -->
      <div class="mt-8 bg-white rounded-lg shadow-sm p-12">
        <h2 class="text-2xl font-bold mb-6">Erstelle einen gemeinsamen Trip!</h2>
        <p class="mb-4">
          Mit travello wird die Reiseplanung in der Gruppe einfacher gestaltet: Keine endlosen Chats, keine Missverständnisse – stattdessen werden eure Wünsche gebündelt, Inspiration entdecken, Ideen sammeln, abstimmen und automatisch einen praktikablen Tagesplan erstellen. Verschafft euch mit travello einen klaren Überblick über die besten Spots und gestaltet eine Planung, die wirklich zu euch passt!
        </p>
      </div>

     

      <!-- App Screenshots im Layout wie in ProjectsGrid -->
      <div class="mt-12 max-w-6xl mx-auto">
        
        <!-- Grid ähnlich wie in ProjectsGrid.vue -->
        <div class="grid grid-cols-1 md:grid-cols-6 gap-6" style="grid-template-rows: auto auto;">
          <!-- Obere Reihe: Logo-Screen (breiter) und Inspirationsseite -->
          <div class="md:col-span-4 md:row-span-1 bg-white rounded-lg overflow-hidden h-full">
            <img src="/images/projects/travello/Startscreen.png" alt="Travello Startbildschirm" class="w-full h-full object-cover" onerror="this.src='/images/placeholder.jpg'" />
          </div>
          
          <!-- Rechte Seite: Screenshot über 2 Reihen -->
          <div class="md:col-span-2 md:row-span-1 bg-white rounded-lg overflow-hidden h-full">
            <img src="/images/projects/travello/Inspiration.png" alt="Travello Inspirationsseite" class="w-full h-full object-cover" onerror="this.src='/images/placeholder.jpg'" />
          </div>
          
          <!-- Untere Reihe: Zwei gleichgroße Screenshots nebeneinander -->
          <div class="md:col-span-2 bg-white rounded-lg overflow-hidden aspect-square">
            <img src="/images/projects/travello/Abstimmung.png" alt="Travello Detailansicht" class="w-full h-full object-cover" onerror="this.src='/images/placeholder.jpg'" />
          </div>
          
          <div class="md:col-span-4 md:row-span-1 bg-white rounded-lg overflow-hidden h-full">
            <img src="/images/projects/travello/drei-Freunde.png" alt="Travello Nutzer" class="w-full h-full object-cover" onerror="this.src='/images/placeholder.jpg'" />
          </div>
        </div>
      </div>

      <!-- Erlerntes -->
      <div class="mt-12 bg-white rounded-lg shadow-sm p-12">
        <h2 class="text-2xl font-bold mb-6">Erlerntes & genutztes</h2>
        <!-- <p class="mb-6">
          Mit travello wird die Reiseplanung in der Gruppe einfacher gestaltet: Keine endlosen Chats, keine Missverständnisse – stattdessen werden eure Wünsche gebündelt, Inspiration entdecken, Ideen sammeln, abstimmen und automatisch einen praktikablen Tagesplan erstellen. Verschafft euch mit travello einen klaren Überblick über die besten Spots und gestaltet eine Planung, die wirklich zu euch passt!
        </p> -->
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
         
          <div>
            <h3 class="font-bold mb-2">Einführung eines Design-Tagebuchs</h3>
            <p class="text-sm">Mit der Einführung eines Design-Tagebuchs schufen wir eine klare Dokumentation aller Prozessschritte & Designentscheidungen.</p>
          </div>
          <div>
            <h3 class="font-bold mb-2">Erstellung einer Component Library</h3>
            <p class="text-sm">Um den wachsenden Prototyp übersichtlich und einheitlich zu halten, entwickelten wir eine klar organisierte Component Library.</p>
          </div>
          <div>
            <h3 class="font-bold mb-2">Nutzerorientierter Design-Prozess</h3>
            <p class="text-sm">Durch intensive Nutzerbefragungen haben wir gelernt, wie wichtig die Einbeziehung der Zielgruppe in jeder Phase ist.</p>
          </div>
        </div>
      </div>

      <!-- Nächstes Projekt -->
<div class="mt-12 bg-white rounded-lg shadow-sm p-12 pb-16 relative">
  <div class="flex justify-between items-end">
    <div>
      <h2 class="text-5xl font-bold text-black">Nächstes Projekt</h2>
      <h3 class="text-2xl font-medium text-green-700 mt-10">Celestial Bodies</h3>
      <p class="text-lg text-gray-700 mt-2">Interaktives Ausstellungskonzept</p>
      
      <!-- Tags -->
      <div class="flex gap-2 mt-4">
        <span class="bg-black text-white text-xs px-2 py-1 rounded-full">Arduino</span>
        <span class="bg-black text-white text-xs px-2 py-1 rounded-full">Interaction</span>
        <span class="bg-black text-white text-xs px-2 py-1 rounded-full">Exhibition</span>
      </div>
    </div>
    <NuxtLink to="/projects/celestial-bodies" class="project-arrow-link text-white w-12 h-12 rounded-full transition flex items-center justify-center">
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

// YouTube-Video URL mit Autoplay-Parameter
const videoSrc = computed(() => {
  return videoPlaying.value 
    ? 'https://www.youtube.com/embed/e4DJAY-LbLo?autoplay=1&rel=0' 
    : '';
});

// Funktion zum Starten des Videos
const startVideo = () => {
  videoPlaying.value = true;
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

/* Styling für Team-Links */
.team-link {
  color: #2f855a; /* Grüne Farbe, passend zum Rest deiner Seite */
  transition: color 0.3s;
  text-decoration: none;
}

.team-link:hover {
  color: #1c5337; /* Dunkleres Grün beim Hover */
  text-decoration: underline;
}

/* Styling für den Video-Container */
.video-container {
  height: 0;
  padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
  position: relative;
}

.video-container img,
.video-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Footer-Divider Styles (aus InternshipNotice.vue übernommen) */
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
  background-color: #e2e8f0; /* Ein dezentes Grau */
  margin-bottom: 0.75rem;
  margin-left: 32px;
  margin-right: 32px;

}

.designed-by {
  font-size: 0.75rem;
  color: #94a3b8; /* Ein dezentes Grau für den Text */
  font-weight: 400;
}

/* Hover-Effekt für den Projekt-Pfeil */
.project-arrow-link {
  background-color: black; /* Standardfarbe: schwarz */
  transition: all 0.3s ease; /* Sanfte Übergänge für alle Eigenschaften */
}

.project-arrow-link:hover {
  background-color: #2f855a; /* Grün beim Hover (var(--color-green)) */
}

.project-arrow-link .arrow-icon {
  transition: transform 0.3s ease; /* Sanfte Rotation */
}

.project-arrow-link:hover .arrow-icon {
  transform: rotate(45deg); /* 45 Grad Drehung beim Hover */
}
</style>