<template>
  <div class="absolute top-0 w-2/4 h-20 flex items-center rounded-full bg-clip-padding backdrop-filter backdrop-blur-md bg-opacity-50 border border-gray-100 justify-center">

      <ul class="flex justify-end">
        <li>
          <nuxt-link
            to="/"
            class="px-10 py-2 underline-offset-4 underline decoration-sky-500"
            >APs</nuxt-link
          >
          <nuxt-link to="#" class="px-10 py-2">Stages</nuxt-link>
          <nuxt-link to="#about" class="px-10 py-2">Veille technologique</nuxt-link>
          <nuxt-link to="../pages/cv.vue" class="px-4 mx-4 py-2 bg-gray-100 text-black rounded-md">Cv</nuxt-link>
        </li>
      </ul>
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="css"></style>
