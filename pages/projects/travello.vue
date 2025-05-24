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

      <!-- Logo und Hauptbild Bereich (ähnlich wie im Screenshot) -->
      <div class="mt-8 grid grid-cols-1 md:grid-cols-12 gap-6">
        
        <!-- Screenshot rechte Seite -->
        <div class="md:col-span-12 bg-white rounded-lg overflow-hidden h-full">
          <img src="/images/projects/travello-titelbild.jpg" alt="travello App Screenshot" class="w-full h-full object-cover" />
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
        <h2 class="text-2xl font-bold mb-6">Erlerntes</h2>
        <p class="mb-6">
          Mit travello wird die Reiseplanung in der Gruppe einfacher gestaltet: Keine endlosen Chats, keine Missverständnisse – stattdessen werden eure Wünsche gebündelt, Inspiration entdecken, Ideen sammeln, abstimmen und automatisch einen praktikablen Tagesplan erstellen. Verschafft euch mit travello einen klaren Überblick über die besten Spots und gestaltet eine Planung, die wirklich zu euch passt!
        </p>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-8">
          <div class="bg-gray-100 p-4 rounded-lg">
            <h3 class="font-bold mb-2">Nutzerorientierter Design-Prozess</h3>
            <p class="text-sm">Durch intensive Nutzerbefragungen haben wir gelernt, wie wichtig die Einbeziehung der Zielgruppe in jeder Phase ist.</p>
          </div>
          <div class="bg-gray-100 p-4 rounded-lg">
            <h3 class="font-bold mb-2">Gruppenentscheidungen effektiv gestalten</h3>
            <p class="text-sm">Die Entwicklung von demokratischen Abstimmungsmechanismen verhindert Konflikte und steigert die Zufriedenheit.</p>
          </div>
          <div class="bg-gray-100 p-4 rounded-lg">
            <h3 class="font-bold mb-2">Balance zwischen Struktur und Flexibilität</h3>
            <p class="text-sm">Ein guter Reiseplan bietet Orientierung, lässt aber auch Raum für spontane Entscheidungen.</p>
          </div>
        </div>
      </div>

      <!-- Weitere Projekte -->
      <div class="mt-12 bg-white rounded-lg shadow-sm p-12">
        <h2 class="text-2xl font-bold mb-6">Weitere Projekte</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          <!-- Celestial Bodies -->
          <div class="overflow-hidden rounded-lg shadow-sm relative group h-64">
            <img src="/images/projects/CelestialBodies-titelbild.jpg" alt="Celestial Bodies" class="w-full h-full object-cover transition-transform duration-500 scale-110 group-hover:scale-120" style="object-position: center 25%;" />
            <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-black/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            <div class="absolute bottom-0 left-0 p-4 text-white z-10">
              <div class="opacity-0 group-hover:opacity-100 transition-opacity duration-500">
                <h3 class="text-xl font-bold">Celestial Bodies</h3>
                <p class="text-sm font-medium opacity-90">Interaktives Ausstellungskonzept</p>
              </div>
            </div>
            <NuxtLink to="/projects/celestial-bodies" class="absolute inset-0 z-20"></NuxtLink>
          </div>

          <!-- Focal -->
          <div class="overflow-hidden rounded-lg shadow-sm relative group h-64">
            <img src="/images/projects/Focal-titelbild.jpg" alt="Focal" class="w-full h-full object-cover transition-transform duration-500 scale-110 group-hover:scale-120" />
            <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-black/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            <div class="absolute bottom-0 left-0 p-4 text-white z-10">
              <div class="opacity-0 group-hover:opacity-100 transition-opacity duration-500">
                <h3 class="text-xl font-bold">Focal</h3>
                <p class="text-sm font-medium opacity-90">Konzept für räumliches arbeiten</p>
              </div>
            </div>
            <NuxtLink to="/projects/focal" class="absolute inset-0 z-20"></NuxtLink>
          </div>

          <!-- comigo -->
          <div class="overflow-hidden rounded-lg shadow-sm relative group h-64">
            <img src="/images/projects/comigo-titelbild.jpg" alt="comigo" class="w-full h-full object-cover transition-transform duration-500 scale-110 group-hover:scale-120" />
            <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-black/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            <div class="absolute bottom-0 left-0 p-4 text-white z-10">
              <div class="opacity-0 group-hover:opacity-100 transition-city duration-500">
                <h3 class="text-xl font-bold">comigo</h3>
                <p class="text-sm font-medium opacity-90">Design-Sprint</p>
              </div>
            </div>
            <NuxtLink to="/projects/comigo" class="absolute inset-0 z-20"></NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// Keine externen Komponenten nötig, da alles inline ist
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
</style>