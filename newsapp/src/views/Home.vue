<template>
  <div class="mx-50">
    <div class="absolute top-0 left-0 w-full h-[450px] bg-black z-[-1]"></div>
    <Navbar />

    <div class="mt-20">
      <Upperbar />
      <Upperarea />

      <div class="grid grid-cols-3 mt-5 gap-20">
        <div class="col-span-2">
          <Latestnews :articles="articles" :loading="isLoading" :error="error" />
        </div>

        <div class="bg-gray-150">
          <Trend :articles="articles" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'

import Upperbar from '../components/Upperbar.vue'
import Upperarea from '../components/Upperarea.vue'
import Latestnews from '../components/Latestnews.vue'
import Trend from '../components/Trend.vue'
import Navbar from '../components/Navbar.vue'

// Haber verisi
const articles = ref([])
const isLoading = ref(true)
const error = ref(null)

const fetchNews = async () => {
  try {
    const response = await axios.get('https://newsapi.org/v2/everything', {
      params: {
        q: 'apple',
        from: '2025-04-07',
        to: '2025-04-07',
        sortBy: 'popularity',
        apiKey: '98b252020f1740c08a5b52b91c856c6a'
      }
    })
    articles.value = response.data.articles
  } catch (err) {
    error.value = err.message
  } finally {
    isLoading.value = false
  }
}

onMounted(() => {
  fetchNews()
  console.log('Articles:', articles)
})
</script>
