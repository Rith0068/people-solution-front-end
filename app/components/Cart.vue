<script setup>
import axios from 'axios';
const key = "3ef60c49e6bed13eb14fa7de1460f5ca1a58c348cf1a2882dd52def6d0868bd0e2992eaae2608ba54902018c4a746f2cde3aab4767380899c20d5f689d67dabf7c68b7272c94373ea59ecf96be4f7c5bd7cf4ebb5ff76ed457f8dd2b63d82f2dba9fc1e1a69658e34a9c84a86e02e03fad521c1ee921a0cd19da5ce135b57eea"
const jobs = await axios.get('http://localhost:1337/api/carts',{
  headers: {
    Authorization : `Bearer ${key}`
  }
})
const properties = jobs.data.data;
</script>



<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 px-4 w-[1260px]">
    <div
      v-for="property in properties.slice(0, 3)"
      :key="property.id"
      class="bg-white rounded-2xl shadow-lg hover:shadow-xl overflow-hidden transition-all duration-300 hover:-translate-y-1 flex flex-col"
    >
      <!-- Image -->
      <div class="overflow-hidden">
        <img
          src="@/assets/image/technology.jpg"
          :alt="property.distriction"
          class="w-full h-[200px] object-cover transition-transform duration-500 hover:scale-105"
        />
      </div>

      <!-- Content -->
      <div class="flex flex-col flex-1 p-4 gap-3">
        <!-- Date -->
        <p class="text-sm text-gray-500 flex items-center gap-2">
          <i class="fa-regular fa-calendar"></i>
          {{ property.date }}
        </p>

        <!-- Title -->
        <p class="text-[17px] font-medium text-gray-800 leading-snug line-clamp-2">
          {{ property.distriction }}
        </p>

        <!-- Button pushed to bottom -->
        <div class="mt-auto">
          <NuxtLink to="/services" 

            class="inline-flex items-center justify-center px-5 py-2 bg-yellow-400 text-white text-sm font-semibold rounded-lg
                   shadow-md hover:bg-yellow-500 hover:shadow-yellow-400/50
                   hover:-translate-y-0.5 active:scale-95
                   transition-all duration-200"
          >
            READ MORE
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>