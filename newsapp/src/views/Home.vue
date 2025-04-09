<template>
  <div>
    <!-- Arka plan -->
    <div class="absolute top-0 left-0 w-full h-[450px] bg-black z-[-1]"></div>

    <div class="max-w-7xl mx-auto px-4 space-y-10">
      <!-- Navbar ve üst bileşenler -->
      <Navbar />
      <Upperbar />
      <Upperarea />

      <!-- İçerik alanı -->
      <div class="grid grid-cols-1 lg:grid-cols-3 mt-8 gap-8">
        <!-- Son Haberler (2/3 genişlik) -->
        <div class="lg:col-span-2">
          <Latestnews :articles="articles" :loading="isLoading" :error="error" />
        </div>

        <!-- Trendler (1/3 genişlik) -->
        <div class="bg-gray-100 p-4 rounded-lg shadow-md">
          <Trend :articles="articles" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'

// Bileşenler
import Navbar from '../components/Navbar.vue'
import Upperbar from '../components/Upperbar.vue'
import Upperarea from '../components/Upperarea.vue'
import Latestnews from '../components/Latestnews.vue'
import Trend from '../components/Trend.vue'

// Reaktif değişkenler
const articles = ref([])
const isLoading = ref(false)
const error = ref(null)
const searchQuery = ref('apple')

// API ayarları
const API_KEY = '98b252020f1740c08a5b52b91c856c6a'
const BASE_URL = 'https://newsapi.org/v2/everything'

// Sayfa yüklendiğinde haberleri getir
onMounted(() => {
  fetchNews()
})

// Haberleri çekme fonksiyonu
const fetchNews = async () => {
  isLoading.value = true
  error.value = null
  try {
    const fromDate = '2025-04-08'
    const toDate = '2025-04-08'
    const response = await axios.get(BASE_URL, {
      params: {
        q: searchQuery.value,
        from: fromDate,
        to: toDate,
        sortBy: 'popularity',
        apiKey: API_KEY,
      },
    })
    articles.value = response.data.articles
  } catch (err) {
    console.error('Error fetching news:', err)
    error.value = err.message || 'Haberler alınırken bir hata oluştu.'
  } finally {
    isLoading.value = false
  }
}
</script>

<style scoped>
/* Gerekirse özel stiller buraya eklenebilir */
</style>
