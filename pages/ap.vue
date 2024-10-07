<template>
    <section class="py-12 bg-gray-100">
      <div class="container mx-auto px-4">
        <h1 class="text-4xl text-center mb-10 text-gray-800">Mon Portfolio</h1>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <div 
            class="relative overflow-hidden rounded-lg shadow-lg transform transition duration-300 hover:-translate-y-2"
            v-for="(project, index) in projects" 
            :key="index"
          >
            <img 
              :src="project.image" 
              :alt="project.title" 
              class="w-full h-auto transform transition duration-300 hover:scale-110"
            />
            <div class="absolute inset-0 bg-black bg-opacity-70 opacity-0 transition-opacity duration-300 flex flex-col justify-center items-center text-center p-4 hover:opacity-100">
              <h3 class="text-2xl text-white mb-2">{{ project.title }}</h3>
              <p class="text-white mb-4">{{ project.description }}</p>
              <a 
                :href="project.link" 
                target="_blank" 
                class="px-4 py-2 bg-orange-500 text-white rounded hover:bg-orange-600 transition-colors duration-300"
              >
                Voir le projet
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>
    
  </template>
  
  <script>
  export default {
    data() {
      return {
        projects: [
          {
            title: 'Projet 1',
            description: 'Description du projet 1.',
            image: '../assets/images/kaizen.png',
            link: 'https://lien-du-projet1.com'
          },
          {
            title: 'Projet 2',
            description: 'Description du projet 2.',
            image: '/images/projet2.jpg',
            link: 'https://lien-du-projet2.com'
          },
          {
            title: 'Projet 3',
            description: 'Description du projet 3.',
            image: '/images/projet3.jpg',
            link: 'https://lien-du-projet3.com'
          },
          {
            title: 'Projet 4',
            description: 'Description du projet 4.',
            image: '/images/projet4.jpg',
            link: 'https://lien-du-projet4.com'
          }
        ]
      }
    }
  }
  </script>
*  