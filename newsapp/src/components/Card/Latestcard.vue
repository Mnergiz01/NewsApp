<template>
    <div>
      <!-- Router-link ile yönlendirme -->
      <router-link to="/details" class="block">
        <img
          src="@/assets/Frame 12.png"
          alt="Image"
          class="transition-transform duration-300 transform hover:scale-105 cursor-pointer"
        />
      </router-link>
    </div>
  </template>
  
  <style scoped>
  /* Büyüme efekti */
  img {
    transition: transform 0.3s ease;
  }
  </style>
  