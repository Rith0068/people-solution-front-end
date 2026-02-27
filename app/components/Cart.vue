<script setup>
import axios from 'axios';
const key = "5cfebb07d4c1eea7806b3407c1e8de1b0b7fd46fccd8c4c582cf7edb4968beee98f9112e8a022f0d657138f6701dfeb78b78303c70378f8948d7f151a17564894c647bd9314b857aa906a7b6297d08fa6fa73e52cd52d1abe282c42626555b2ade9be92a425fb93bfc98c2d14a37928deee3bbf98a512b231ec6c99800bc0748"
const jobs = await axios.get('http://localhost:1337/api/carts',{
  headers: {
    Authorization : `Bearer ${key}`
  }
})
const properties = jobs.data.data
</script>



<template>
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 px-4 w-315">
    <div
      v-for="property in properties.slice(0, 3)"
      :key="property.id"
      class="bg-white rounded-2xl shadow-lg hover:shadow-xl overflow-hidden transition-all duration-300 hover:-translate-y-1 flex flex-col"
    >
      <!-- Image -->
      <div class="overflow-hidden">
        <img
          src="@/assets/images/technology.jpg"
          :alt="property.distriction"
          class="w-full h-50 object-cover transition-transform duration-500 hover:scale-105"
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
          <NuxtLink
            to=""
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