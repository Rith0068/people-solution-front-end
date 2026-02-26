<script setup>
import axios from 'axios';

const key = "16585b8481e5a15faac681095cb0527a5d6a3d228e25f41a6531dd5eb647abe9298f669875331c0065a4080845edd51a4d953e4a3319aea64217c93db6ef4048325c00a189f7be983be198fa0212248bf98647292f34fd30f3e75f0f5403b7f5927059b2bc8bc4bcbe8bf632f631f6ce0993b38a580dc12a8fab7a786cc4b0e5";

const res = await axios.get('http://localhost:1337/api/job-accountings', {
  headers: {
    Authorization: `Bearer ${key}`
  }
});

const jobs = res.data.data;
</script>

<template>  
  <div>
    <div class="flex flex-wrap gap-6">
        <div v-for="job in jobs.slice(0)" :key="job.id" class="bg-white rounded-2xl shadow-lg hover:shadow-2xl w-[260px] overflow-hidden hover:-translate-y-2 transition-all duration-300 border border-gray-100 group">

 
        <div class="overflow-hidden w-full h-[180px] bg-slate-200">
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