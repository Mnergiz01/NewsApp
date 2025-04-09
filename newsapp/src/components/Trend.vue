<template>
    <div class="p-6">
      <!-- Başlık ve Buton -->
      <div class="flex flex-row justify-between items-center mb-6">
        <h1 class="text-xl font-semibold text-gray-900">Trending Headlines</h1>
        <button class="text-blue-500 hover:text-blue-700 font-medium transition-colors duration-300">
          View All
        </button>
      </div>
  
      <!-- Kartlar -->
      <div class="flex flex-col gap-6">
        <Trendingcard />
        <Trendingcard />
        <Trendingcard />
        <Trendingcard />
        <Trendingcard />
        <Trendingcard />
        <Trendingcard />
        <Trendingcard />
      </div>
    </div>
  </template>
  
  <script setup>
  import Trendingcard from './Card/Trendingcard.vue'
  </script>
  
  <style scoped>
  /* Buton Hover */
  
  </style>
  