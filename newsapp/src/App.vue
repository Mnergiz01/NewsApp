<template>
  <div>
    <!-- Siyah arka plan -->
    <div class="absolute top-0 left-0 w-full h-[450px] bg-black z-[-1]"></div>

    <div class="min-h-screen flex flex-col mx-82 z-20 relative">
      <div class="flex-1">
        <Navbar />
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
