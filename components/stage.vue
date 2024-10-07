<!-- components/Stage.vue -->
<template>
    <section id="stage" class="py-12 bg-white">
      <div class="max-w-5xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-6">Mon Expérience de Stage</h2>
        <div class="mb-8">
          <h3 class="text-2xl font-semibold mb-4 flex items-center justify-center">
            <svg class="w-6 h-6 text-green-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c1.657 0 3 1.343 3 3v4a3 3 0 01-6 0v-4c0-1.657 1.343-3 3-3z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5.121 17.804A4 4 0 0012 15a4 4 0 006.879-2.804M15 19h6M9 19h6" />
            </svg>
            Développeur Front-End chez Les Jolies Mancelles
          </h3>
          <p class="text-gray-700 mb-4 text-center">
            J'ai effectué mon stage de 6 mois chez <strong>Les Jolies Mancelles</strong>, un salon de beauté renommé situé au Mans. Mon rôle principal était de concevoir et de développer un site internet moderne et fonctionnel pour l'entreprise, afin d'améliorer sa présence en ligne et d'attirer davantage de clients.
          </p>
        </div>
  
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-2 text-center">Mes Tâches</h4>
          <ul class="list-disc list-inside text-gray-700">
            <li class="flex items-center mb-2">
              <svg class="w-5 h-5 text-green-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              Conception et développement du site internet en utilisant Vue.js et Nuxt.js.
            </li>
            <li class="flex items-center mb-2">
              <svg class="w-5 h-5 text-green-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              Création d'une interface utilisateur intuitive et responsive pour une expérience optimale sur tous les appareils.
            </li>
            <li class="flex items-center mb-2">
              <svg class="w-5 h-5 text-green-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              Intégration des fonctionnalités de réservation en ligne et de gestion des rendez-vous.
            </li>
            <li class="flex items-center mb-2">
              <svg class="w-5 h-5 text-green-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              Optimisation du référencement (SEO) pour améliorer la visibilité du salon sur les moteurs de recherche.
            </li>
            <li class="flex items-center mb-2">
              <svg class="w-5 h-5 text-green-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              Collaboration avec l'équipe de marketing pour aligner le design du site avec l'identité visuelle de l'entreprise.
            </li>
          </ul>
        </div>
  
        <!-- Galerie d'Images -->
        <div>
          <h4 class="text-xl font-semibold mb-4 flex items-center justify-center">
            <svg class="w-6 h-6 text-green-500 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4h16v16H4V4z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h8M8 16h8M8 8h8" />
            </svg>
            Galerie
          </h4>
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
            <div v-for="(image, index) in stageImages" :key="index" class="overflow-hidden rounded-lg shadow-lg">
              <img 
                :src="image" 
                alt="Image du Stage chez Les Jolies Mancelles" 
                loading="lazy" 
                class="w-full h-60 object-cover transform transition-transform duration-300 hover:scale-105"
              />
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const stageImages = ref([
    '/images/stage/stage1.jpg',
    '/images/stage/stage2.jpg',
    '/images/stage/stage3.jpg',
    '/images/stage/stage4.jpg'
  ])
  </script>
  
  <style scoped>
  /* Styles personnalisés si nécessaire */
  </style>
  