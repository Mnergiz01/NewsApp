<template>
    <div>
      <!-- Başlık ve Çizgi -->
      <div class="flex items-center mb-6">
        <h1 class="text-2xl font-bold mx-8 my-4">Latest News</h1>
        <hr class="flex-grow border-t border-gray-400 mx-4" />
      </div>
  
      <!-- Kartlar -->
      <div class="grid grid-cols-2 gap-5 mx-8">
        <Latestcard />
        <Latestcard />
        <Latestcard />
        <Latestcard />
        <Latestcard />
        <Latestcard />
        <Latestcard />
        <Latestcard />
      </div>
  
      <!-- View All Butonu -->
      <div class="flex justify-center mt-8">
        <button class="bg-blue-500 hover:bg-blue-600 text-white px-6 py-3 rounded transition duration-300">
          View All
        </button>
      </div>
    </div>
  </template>
  
  <script setup>
  import Latestcard from './Card/Latestcard.vue'
  </script>
  