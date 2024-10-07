<!-- pages/veille.vue -->
<template>
    <div class="min-h-screen bg-gray-100 p-6">
      <div class="max-w-5xl mx-auto bg-white shadow-md rounded-lg overflow-hidden">
        <!-- En-tête de la Page -->
        <header class="bg-indigo-600 text-black p-6">
          <h1 class="text-3xl font-bold">Veille Technologique</h1>
          <p class="text-lg mt-2">Les technologies que je souhaite explorer et maîtriser prochainement.</p>
        </header>
  
        <!-- Contenu Principal -->
        <section class="p-6">
          <!-- Technologie 1 : Nuxt.js -->
          <div class="mb-8">
            <h2 class="text-2xl font-semibold mb-4 flex items-center">
              <svg class="w-6 h-6 text-indigo-600 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6l4 2" />
              </svg>
              Nuxt.js
            </h2>
            <p class="text-gray-700 mb-4">
              Nuxt.js est un framework basé sur Vue.js qui facilite le développement d'applications web universelles. Il offre une structure robuste pour créer des applications performantes avec une excellente optimisation SEO.
            </p>
            <ul class="list-disc list-inside text-gray-700">
              <li>Rendu côté serveur (SSR) pour de meilleures performances et SEO.</li>
              <li>Système de routage automatique basé sur le fichier.</li>
              <li>Support intégré pour la gestion de l'état avec Vuex.</li>
              <li>Facilité d'intégration avec des CMS et des API externes.</li>
            </ul>
          </div>
  
          <!-- Technologie 2 : Laravel -->
          <div class="mb-8">
            <h2 class="text-2xl font-semibold mb-4 flex items-center">
              <svg class="w-6 h-6 text-indigo-600 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m2 0a2 2 0 110 4H7a2 2 0 110-4h2" />
              </svg>
              Laravel
            </h2>
            <p class="text-gray-700 mb-4">
              Laravel est un framework PHP élégant et puissant destiné au développement d'applications web. Il offre une syntaxe expressive et fournit des outils robustes pour simplifier les tâches courantes telles que l'authentification, la gestion des bases de données et le routage.
            </p>
            <ul class="list-disc list-inside text-gray-700">
              <li>Moteur de template Blade pour des vues dynamiques.</li>
              <li>ORM Eloquent pour une interaction simplifiée avec la base de données.</li>
              <li>Système de migration pour la gestion des schémas de base de données.</li>
              <li>Support natif pour les tests unitaires et fonctionnels.</li>
            </ul>
          </div>
  
          <!-- Autres Technologies -->
          <div>
            <h2 class="text-2xl font-semibold mb-4 flex items-center">
              <svg class="w-6 h-6 text-indigo-600 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6l4 2" />
              </svg>
              Autres Technologies en Perspective
            </h2>
            <ul class="list-disc list-inside text-gray-700">
              <li>**GraphQL** : Pour des API flexibles et efficaces.</li>
              <li>**Docker** : Pour la containerisation et la gestion des environnements de développement.</li>
              <li>**Tailwind CSS** : Pour un stylisme rapide et réactif avec des classes utilitaires.</li>
              <li>**React** : Pour diversifier les compétences en frameworks JavaScript.</li>
            </ul>
          </div>
        </section>
  
        <!-- Section Conclusion -->
        <footer class="bg-gray-100 p-6">
          <p class="text-center text-gray-600">
            Je suis constamment à la recherche de nouvelles technologies à apprendre pour améliorer mes compétences et offrir des solutions innovantes. Restez connecté pour suivre mon évolution !
          </p>
        </footer>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'VeilleTechnologique',
  }
  </script>
  
  <style scoped>
  /* Styles personnalisés si nécessaire */
  </style>
  