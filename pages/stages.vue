<!-- pages/stage.vue -->
<template>
    <div class="min-h-screen bg-gray-100 p-6">
      <div class="max-w-5xl mx-auto bg-white shadow-md rounded-lg overflow-hidden">
        <!-- En-tête de la Page -->
        <header class="bg-green-600 text-white p-6">
          <h1 class="text-3xl font-bold">Mon Expérience de Stage</h1>
          <p class="text-lg mt-2">Découvrez mon stage chez <strong>Les Jolies Mancelles</strong></p>
        </header>
  
        <!-- Contenu Principal -->
        <section class="p-6">
          <!-- Présentation du Stage -->
          <div class="mb-8">
            <h2 class="text-2xl font-semibold mb-4 flex items-center">
              <svg class="w-6 h-6 text-green-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c1.657 0 3 1.343 3 3v4a3 3 0 01-6 0v-4c0-1.657 1.343-3 3-3z" />
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5.121 17.804A4 4 0 0012 15a4 4 0 006.879-2.804M15 19h6M9 19h6" />
              </svg>
              Développeur Front-End
            </h2>
            <p class="text-gray-700 mb-4">
              J'ai effectué mon stage de 6 mois chez <strong>Les Jolies Mancelles</strong>, un salon de beauté renommé situé au Mans. Mon rôle principal était de concevoir et de développer un site internet moderne et fonctionnel pour l'entreprise, afin d'améliorer sa présence en ligne et d'attirer davantage de clients.
            </p>
          </div>
  
          <!-- Tâches et Réalisations -->
          <div class="mb-8">
            <h3 class="text-xl font-semibold mb-2">Mes Tâches</h3>
            <ul class="list-disc list-inside text-gray-700">
              <li>Conception et développement du site internet en utilisant Vue.js et Nuxt.js.</li>
              <li>Création d'une interface utilisateur intuitive et responsive pour une expérience optimale sur tous les appareils.</li>
              <li>Intégration des fonctionnalités de réservation en ligne et de gestion des rendez-vous.</li>
              <li>Optimisation du référencement (SEO) pour améliorer la visibilité du salon sur les moteurs de recherche.</li>
              <li>Collaboration avec l'équipe de marketing pour aligner le design du site avec l'identité visuelle de l'entreprise.</li>
            </ul>
          </div>
  
          <!-- Galerie d'Images -->
          <div>
            <h3 class="text-xl font-semibold mb-4 flex items-center">
              <svg class="w-6 h-6 text-green-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4h16v16H4V4z" />
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h8M8 16h8M8 8h8" />
              </svg>
              Galerie
            </h3>
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
              <div v-for="(image, index) in stageImages" :key="index" class="overflow-hidden rounded-lg shadow-lg">
                <img 
                  :src="image" 
                  alt="Image du Stage chez Les Jolies Mancelles" 
                  loading="lazy" 
                  class="w-full h-60 object-cover transform transition-transform duration-300 hover:scale-105"
                >
              </div>
            </div>
          </div>
        </section>
  
        <!-- Footer de la Page -->
        <footer class="bg-gray-100 p-6">
          <p class="text-center text-gray-600">
            Merci d'avoir consulté mon expérience de stage chez <strong>Les Jolies Mancelles</strong>. N'hésitez pas à me contacter pour plus d'informations ou pour discuter de collaborations futures !
          </p>
        </footer>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'StagePage',
    data() {
      return {
        stageImages: [
            '~/assets/images/photolio.png',
            '~/assets/images/stage/stage2.jpg',
            '~/assets/images/stage/stage3.jpg',
            '~/assets/images/stage/stage4.jpg'
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  /* Styles personnalisés si nécessaire */
  </style>
  