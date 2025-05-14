// components/InternshipNotice.vue

<template>
  <section class="relative bg-white rounded-lg shadow-sm p-12 mx-auto max-w-9xl">
    <!-- Hero Content -->
    <h1 class="text-5xl font-bold mb-12">
      Das War's!
    </h1>

    <p class="max-w-2xl text-xl font-medium text-gray-800 text-left leading-relaxed mt-32 mb-6">
      Ab Herbst '25 suche ich nach einer Praktikumsstelle um mein Wissen zu erweitern. Melde dich gerne bei mir!
    </p>

    <!-- Kontakt Links -->
    <div class="absolute bottom-12 right-12 flex items-center space-x-4 mb-6">
      <!-- E-Mail Link -->
      <a href="mailto:eric.hochstatter@mail.de" class="contact-link flex items-center">
        <svg class="w-5 h-5 mr-1" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"></path>
          <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"></path>
        </svg>
        <span>E-Mail</span>
      </a>

      <!-- LinkedIn Link -->
      <a href="https://www.linkedin.com/in/eric-hochstatter-91b368358/" target="_blank" rel="noopener noreferrer" class="contact-link flex items-center">
        <svg class="w-5 h-5 mr-1" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
        </svg>
        <span>LinkedIn</span>
      </a>
    </div>

    <!-- Trennstrich und "Designed by"-Hinweis -->
    <div class="footer-divider">
      <div class="divider"></div>
      <p class="designed-by">Design & Development by Eric Hochstatter © 2025</p>
    </div>
  </section>
</template>

<style scoped>
.highlight {
  color: #2f855a; /* Tailwind's green-800 */
  position: relative;
  text-decoration: underline;
  text-decoration-color: #2f855a;
  text-underline-offset: 4px;
}

.contact-link {
  color: #2f855a;
  transition: all 0.3s;
  font-weight: 500;
}

.contact-link:hover {
  color: #1c5337;
  text-decoration: underline;
}

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
</style>
