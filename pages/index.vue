<template>
  <div>
    <!-- Header -->
    <header class="bg-gray-800 text-white p-4 fixed top-0 w-full z-50">
      <h1 class="text-3xl font-bold text-center">Enzo Portfolio</h1>
      <nav class="mt-4">
        <ul class="flex justify-center space-x-4 f">
          <li><a href="#accueil" class="hover:text-blue-300">Accueil</a></li>
          <li><a href="#projets" class="hover:text-blue-300">Projets</a></li>
          <li><a href="#stages" class="hover:text-blue-300">Stages</a></li>
          <li><a href="#veille" class="hover:text-blue-300">Veille Technologique</a></li>
          <li><a href="#cv" class="hover:text-blue-300">CV</a></li>
        </ul>
      </nav>
    </header>

    <!-- Formulaire de Connexion -->
    <div v-if="!isLoggedIn" class="flex items-center justify-center min-h-screen bg-gray-100">
      <div class="bg-white p-8 rounded-lg shadow-md w-96">
        <h2 class="text-2xl font-bold mb-6 text-center">Connexion</h2>
        <form @submit.prevent="handleLogin">
          <div class="mb-4">
            <label for="username" class="block mb-2">Identifiant</label>
            <input
              type="text"
              v-model="username"
              id="username"
              class="border border-gray-300 p-2 w-full rounded"
              required
            />
          </div>
          <div class="mb-6">
            <label for="password" class="block mb-2">Mot de passe</label>
            <input
              type="password"
              v-model="password"
              id="password"
              class="border border-gray-300 p-2 w-full rounded"
              required
            />
          </div>
          <button type="submit" class="w-full bg-blue-600 text-white p-2 rounded hover:bg-blue-500">
            Se connecter
          </button>
        </form>
        <p v-if="error" class="text-red-500 mt-4">{{ error }}</p>
      </div>
    </div>

    <!-- Contenu Principal -->
    <div v-else>
      <!-- Section Accueil -->
      <section id="accueil" class="min-h-screen flex items-center justify-center bg-orange-100">
        <div class="text-center">
          <h2 class="text-4xl font-semibold mb-4 text-black">Bienvenue sur mon portfolio</h2>
          <p class="text-lg text-black">Voici un aperçu de mes projets et expériences.</p>
        </div>
      </section>

      <!-- Section Projets -->
<section id="projets" class="min-h-screen flex flex-col items-center justify-center bg-blue-200">
  <div class="text-center mb-6">
    <h2 class="text-3xl font-semibold mb-4 text-black">Mes Projets</h2>
  </div>
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4 p-4">
    
    <!-- Projet AP1 -->
    <div class="relative group cursor-pointer" @click="openModal({
        title: 'Projet AP1',
        image: '@/assets/images/ap1.png',
        description: 'L\'objectif de ce projet était de créer un site web WordPress avec une base de données et de le personnaliser selon des critères d\'évaluation spécifiques.',
        tools: 'WordPress, PhpMyAdmin',
        skills: 'Développement Web, Gestion de Base de Données, Personnalisation CMS',
        documentation: 'https://example.com/documentation-projet-ap1',
        screenshots: [
          '@/assets/images/kaizen1.png',
          '@/assets/images/kaizen2.png'
        ],
        workMode: 'En équipe'
      })">
      <img src="../assets/images/ap1.png" alt="Projet AP1" class="w-full h-64 object-cover rounded-lg" />
      <div class="absolute inset-0 bg-black bg-opacity-50 flex flex-col items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300">
        <p class="text-white text-sm">Création d'un site web WordPress personnalisé.</p>
        <p class="text-white text-sm mt-2">Technologies: WordPress, PhpMyAdmin</p>
      </div>
    </div>

    <!-- Projet AP2 -->
    <div class="relative group cursor-pointer" @click="openModal({
        title: 'Projet AP2',
        image: '@/assets/images/github.png',
        description: 'Ce projet, réalisé lors d\'un atelier professionnel au cours de ma première année de BTS SIO, consistait à reproduire un site web en utilisant le CMS de notre choix.',
        tools: 'Framer',
        skills: 'Design UI/UX, Utilisation de CMS, Collaboration en Équipe',
        documentation: 'https://example.com/documentation-projet-ap2',
        screenshots: [
          '@/images/github1.png',
          '@/images/github2.png'
        ],
        workMode: 'En équipe'
      })">
      <img src="../assets/images/sciss.png" alt="Projet AP2" class="w-full h-64 object-cover rounded-lg" />
      <div class="absolute inset-0 bg-black bg-opacity-50 flex flex-col items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300">
        <p class="text-white text-sm">Reproduction d'un site web avec un CMS au choix.</p>
        <p class="text-white text-sm mt-2">Technologies: Framer</p>
      </div>
    </div>

    <!-- Projet AP3 -->
    <div class="relative group cursor-pointer" @click="openModal({
        title: 'Projet AP3',
        image: '@/assets/images/cars.png',
        description: 'Ce site utilise PHP pour générer des pages dynamiques et interactives, permettant aux utilisateurs d\'interagir avec le contenu en temps réel.',
        tools: 'PHP, Bootstrap, PhpMyAdmin',
        skills: 'Programmation PHP, Design Responsive, Gestion de Base de Données',
        documentation: 'https://example.com/documentation-projet-ap3',
        screenshots: [
          '@/assets/images/cars.png',
          '@/assets/images/cars.png'
        ],
        workMode: 'Seul'
      })">
      <img src="@/assets/images/cars.png" alt="Projet AP3" class="w-full h-64 object-cover rounded-lg" />
      <div class="absolute inset-0 bg-black bg-opacity-50 flex flex-col items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300">
        <p class="text-white text-sm">Site dynamique avec PHP et bases de données.</p>
        <p class="text-white text-sm mt-2">Technologies: PHP, Bootstrap, PhpMyAdmin</p>
      </div>
    </div>

    <!-- Projet AP4 -->
    <div class="relative group cursor-pointer" @click="openModal({
        title: 'Projet AP4',
        image: '@/assets/images/enzo-petit.png',
        description: 'Description du Projet AP4',
        tools: 'PHP, Tailwind CSS, PhpMyAdmin',
        skills: 'Développement Frontend, Styling avec Tailwind, Backend PHP',
        documentation: 'https://example.com/documentation-projet-ap4',
        screenshots: [
          '@/images/enzo-petit1.png',
          '@/images/enzo-petit2.png'
        ],
        workMode: 'En équipe'
      })">
      <img src="@/assets/images/ap2.png" alt="Projet AP4" class="w-full h-64 object-cover rounded-lg" />
      <div class="absolute inset-0 bg-black bg-opacity-50 flex flex-col items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300">
        <p class="text-white text-sm">Développement web avancé avec Tailwind CSS.</p>
        <p class="text-white text-sm mt-2">Technologies: PHP, Tailwind CSS, PhpMyAdmin</p>
      </div>
    </div>

    <!-- Projet AP5 -->
    <div class="relative group cursor-pointer" @click="openModal({
        title: 'Projet AP5',
        image: '@/assets/images/nouveau-projet.png',
        description: 'Description du Projet AP5',
        tools: 'React, Redux',
        skills: 'Développement Frontend, Gestion d\'État avec Redux, Intégration API',
        documentation: 'https://example.com/documentation-projet-ap5',
        screenshots: [
          '@/images/nouveau-projet1.png',
          '@/images/nouveau-projet2.png'
        ],
        workMode: 'Seul'
      })">
      <img src="@/assets/images/ap5.png" alt="Projet AP5" class="w-full h-64 object-cover rounded-lg" />
      <div class="absolute inset-0 bg-black bg-opacity-50 flex flex-col items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300">
        <p class="text-white text-sm">à définir</p>
        <p class="text-white text-sm mt-2">à définir</p>
      </div>
    </div>

  </div>
</section>


      <!-- Section Stages -->
      <section id="stages" class="min-h-screen flex flex-col items-center justify-center bg-yellow-100">
        <div class="text-center">
          <h2 class="text-3xl font-semibold mb-4 text-black">Mes Stages</h2>
          <p class="mb-4 text-lg text-black">
            J'ai eu l'opportunité de réaliser un stage chez <strong>"Les jolies Mancelles - 13 Mai au 14 Juin"</strong>, où j'ai conçu un site internet 
            à l'aide d'un CMS Framer. Ce projet m'a permis de mettre en pratique mes compétences en développement web et de travailler 
            sur un projet concret, ce qui a considérablement enrichi mon expérience professionnelle.
          </p>*
          <p class="mb-4 text-lg text-black">
            Le site web que j'ai développé vise à mettre en valeur les produits artisanaux proposés par l'entreprise. Grâce à 
            Framer, j'ai pu créer une interface utilisateur intuitive et esthétiquement plaisante, tout en facilitant la gestion 
            du contenu pour l'équipe de "Les jolies Mancelles". 
          </p>
          <p class="mb-4 text-lg text-black">
            Ce projet m'a également permis d'apprendre à collaborer efficacement avec des clients pour comprendre leurs besoins 
            et transformer leurs idées en une réalité numérique. Je suis fier d'avoir contribué à leur visibilité en ligne.
          </p>
          <p class="mb-4 text-lg text-black">
            Outils : Framer et Figma
          </p>
          <p class="mb-4 text-lg text-red-500">
            Mode de travail : en autonomie en distanciel
          </p>
          <p class="mt-4">
            <a href="https://www.canva.com/design/DAGS7NGDuYI/UAbZvLvxKDOy3glsaFRpJQ/view" target="_blank" rel="noopener" class="text-blue-500 hover:underline">Télécharger le document Technique</a>
        </p>
          
          
          <div class="flex justify-center space-x-4">
            <img src="@/assets/images/mancelles1.png" alt="Capture d'écran du site Les jolies Mancelles" class="w-1/2 rounded-lg shadow-md" />
            <img src="@/assets/images/mancelles2.png" alt="Page de produits Les jolies Mancelles" class="w-1/2 rounded-lg shadow-md" />
          </div>
        </div>
      </section>

      <!-- Section Veille Technologique -->
      <section id="veille" class="min-h-screen flex items-center justify-center bg-violet-200">
        <div class="max-w-5xl mx-auto px-4 text-center">
          <h2 class="text-5xl font-semibold mb-4 text-black">Veille Technologique</h2>
          <p class="text-black text-xl mb-4">
            Dans un monde en constante évolution, il est essentiel de rester à jour avec les nouvelles technologies et tendances. 
            Actuellement, je m'intéresse particulièrement à <strong>Nuxt.js</strong>, un framework puissant pour Vue.js qui facilite le développement de sites web dynamiques et optimisés pour le SEO. 
            En maîtrisant Nuxt.js, je souhaite créer des applications performantes et intuitives qui offrent une expérience utilisateur fluide.
          </p>
          <p class="text-black text-xl">
            Par ailleurs, je suis également attiré par <strong>Laravel</strong>, un framework PHP qui simplifie le développement d'applications web robustes et sécurisées. 
            Grâce à sa syntaxe élégante et à ses fonctionnalités avancées, Laravel me permettra d'améliorer mes compétences en backend tout en construisant des solutions efficaces.
          </p>
          <p class="text-black text-xl">
            En poursuivant ma veille technologique, je suis convaincu que ces compétences me permettront d'être plus polyvalent et de relever de nouveaux défis dans le domaine du développement web.
          </p>
        </div>
      </section>

      

      <section id="cv" class="min-h-screen flex flex-col items-center justify-center bg-green-100">
        <div class="text-center">
            <h2 class="text-3xl font-semibold mb-4 text-black">Mon CV</h2>
            <p class="text-black">Voici mon CV.</p>
            
            <!-- Iframe Canva agrandi -->
            <div style="position: relative; width: 100%; height: 0; padding-top: 180%; padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden; border-radius: 8px; will-change: transform;">
                <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0; margin: 0;"
                    src="https://www.canva.com/design/DAGSihh6PTw/ej0m8Kn6jtBt59bW2_0oPA/view?embed" 
                    allowfullscreen="allowfullscreen" 
                    allow="fullscreen">
                </iframe>
            </div>
            
            <p class="mt-4">
                <a href="https://www.canva.com/design/DAGSihh6PTw/ej0m8Kn6jtBt59bW2_0oPA/view?utm_content=DAGSihh6PTw&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener" class="text-blue-500 hover:underline">Télécharger mon CV</a>
            </p>
        </div>
    </section>
    
    
      
    

      <!-- Footer -->
      <footer class="bg-orange-300 text-white text-center p-4">
        <p>Mon Portfolio</p>
      </footer>

      <!-- Modale pour les Détails des Projets -->
<div v-if="showModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
  <div class="bg-white rounded-lg shadow-lg w-11/12 md:w-3/4 lg:w-1/2 max-h-full overflow-y-auto">
    <div class="flex justify-between items-center p-4 border-b">
      <h3 class="text-2xl font-semibold">Titre du Projet</h3>
      <button @click="closeModal" class="text-gray-600 hover:text-gray-800">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>
    <div class="p-4">
      <img src="@/assets/images/ap1.png" alt="Titre du Projet" class="w-full h-64 object-cover rounded-lg mb-4" />
      <p class="mb-4"><strong>Description:</strong> L'objectif de ce projet était de créer un site web WordPress...</p>
      <p class="mb-4"><strong>Outils Utilisés:</strong> WordPress, PhpMyAdmin</p>
      <p class="mb-4"><strong>Compétences Travaillées:</strong> Développement Web, Gestion de Base de Données</p>
      <p class="mb-4">
        <strong>Production en Ligne / Captures d'Écran:</strong>
      </p>
      <p class="mb-4"><strong>Mode de Travail:</strong> En équipe</p>
    </div>
    <div class="flex justify-end p-4 border-t">
      <button @click="closeModal" class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-500">
        Fermer
      </button>
    </div>
  </div>
</div>

    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

// État de Connexion
const isLoggedIn = ref(false);
const username = ref('');
const password = ref('');
const error = ref('');

// État de la Modale
const showModal = ref(false);
const selectedProject = ref(null);

// Gestion de la Connexion
const handleLogin = () => {
  // Remplacez ces valeurs par vos identifiants souhaités
  const validUsername = 'admin';
  const validPassword = 'password123';

  if (username.value === validUsername && password.value === validPassword) {
    isLoggedIn.value = true;
    // Vérifier si window est défini avant d'utiliser localStorage
    if (typeof window !== 'undefined') {
      localStorage.setItem('isLoggedIn', 'true');
    }
    error.value = '';
  } else {
    error.value = 'Identifiant ou mot de passe incorrect.';
  }
};

// Gestion de la Déconnexion
const logout = () => {
  isLoggedIn.value = false;
  if (typeof window !== 'undefined') {
    localStorage.removeItem('isLoggedIn');
  }
  username.value = '';
  password.value = '';
  error.value = '';
};

// Fonction pour Ouvrir la Modale avec les Détails du Projet
const openModal = (project) => {
  selectedProject.value = project;
  showModal.value = true;
};

// Fonction pour Fermer la Modale
const closeModal = () => {
  showModal.value = false;
  selectedProject.value = null;
};

// Charger l'état de connexion après le montage
onMounted(() => {
  if (typeof window !== 'undefined') {
    isLoggedIn.value = localStorage.getItem('isLoggedIn') === 'true';
  }
});
</script>

<style scoped>
/* Styles supplémentaires si nécessaire */

/* Ajout d'une transition pour la modale */
.fixed {
  transition: opacity 0.3s ease;
}

/* Améliorations de l'apparence de la modale */
.fixed .bg-white {
  animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
