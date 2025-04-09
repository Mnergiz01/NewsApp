<template>
  <div>
    <!-- Siyah arka plan -->
    

    <div class="min-h-screen flex flex-col">
      <div class="flex-1">
        
        <router-view />
      </div>
    </div>

    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
</script>

<style scoped>
/* Şu an ek bir stil gerek yok */
</style>
