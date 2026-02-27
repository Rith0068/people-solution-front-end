<script setup>
import axios from 'axios';
const key = "5cfebb07d4c1eea7806b3407c1e8de1b0b7fd46fccd8c4c582cf7edb4968beee98f9112e8a022f0d657138f6701dfeb78b78303c70378f8948d7f151a17564894c647bd9314b857aa906a7b6297d08fa6fa73e52cd52d1abe282c42626555b2ade9be92a425fb93bfc98c2d14a37928deee3bbf98a512b231ec6c99800bc0748";
const datas = await axios.get('http://localhost:1337/api/job-technologies',{
  headers: {
    Authorization : `Bearer ${key}`
  }
});
const data = datas.data.data;
</script>

<template>
  <div class="">
    <div class="flex flex-wrap gap-6">
        <div v-for="job in data.slice(0, 10)" :key="job.id" class="bg-white rounded-2xl shadow-lg hover:shadow-2xl w-65 overflow-hidden hover:-translate-y-2 transition-all duration-300 border border-gray-100 group">

 
        <div class="overflow-hidden w-full h-45 bg-slate-200">
          <img :src="job.picture || 'https://placehold.co/260x180'" :alt="job.title" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
        </div>

   
        <div class="p-5 flex flex-col gap-2">

     
          <h3 class="text-lg font-bold text-slate-800 leading-tight line-clamp-2 group-hover:text-blue-600 transition-colors duration-200 ">
            {{ job.title }}
          </h3>

          
          <p class="text-sm text-slate-500 flex items-center gap-1.5">
            <span class=""><i class="fa-solid fa-building text-yellow-400  shrink-0"></i></span>
            {{ job.company }}
          </p>

          
          <p class="text-sm text-slate-400 flex items-center gap-1.5">
            <svg class="w-4 h-4 text-yellow-500 shrink-0" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/>
            </svg>
            {{ job.location }}
          </p>

          
          <div class="border-t border-dashed border-gray-200 my-1"></div>

          <div class="flex items-center justify-between">
            <span class="text-sm font-semibold text-green-600 bg-green-50 px-3 py-1 rounded-full">
              {{ job.salary }}
            </span>
            <button class="text-xs font-semibold text-blue-500 hover:text-blue-700 transition-colors">
              View →
            </button>
          </div>

        </div>

      </div>

    </div>
  </div>
</template>