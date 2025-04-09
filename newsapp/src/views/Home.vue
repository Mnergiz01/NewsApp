<template>
  <div class="mx-50">
    <div class="absolute top-0 left-0 w-full h-[450px] bg-black z-[-1]"></div>
    <Navbar/>
    <div class="mt-20">
    <Upperbar/>
    <Upperarea/>
    <di class="grid grid-cols-3 mt-5 gap-20">
      <div class="col-span-2">
        <Latestnews/>
      </div>
      <div class="bg-gray-150">
        <Trend/>
      </div>

    </di>
  </div>
  </div>
  
</template>
<script setup>
import Upperbar from '../components/Upperbar.vue'
import Upperarea from '../components/Upperarea.vue'
import Latestnews from '../components/Latestnews.vue'
import Trend from '../components/Trend.vue'
import Navbar from '../components/Navbar.vue'
</script>
