<!-- pages/cv.vue -->
<template>
    <div class="min-h-screen bg-gray-100 p-4">
      <div class="max-w-7xl mx-auto bg-white shadow-md rounded-lg overflow-hidden">
        <!-- Titre de la Page -->
        <header class="bg-blue-600 text-black p-6">
          <h1 class="text-3xl font-bold">Mon CV</h1>
          <p class="text-lg">Téléchargez mon CV ci-dessous ou visualisez-le directement sur cette page.</p>
        </header>
  
        
        <section class="p-6">
          <div class="flex justify-center mb-4">
            <a href="..\assets\images\CvOralStage.pdf" download class="px-4 py-2 bg-green-500 text-white rounded hover:bg-green-600 transition">
              Télécharger le CV
            </a>
          </div>
          <div class="w-full h-screen md:h-[80vh]">
            <iframe
              src="..\assets\images\CvOralStage.pdf"
              class="w-full h-full border"
              title="CV"
            ></iframe>
          </div>
        </section>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CVPage',
  }
  </script>
  
  <style scoped>
  /* Optionnel : Ajoutez des styles personnalisés si nécessaire */
  </style>
  