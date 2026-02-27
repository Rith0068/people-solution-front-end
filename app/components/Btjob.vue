<script setup>
</script>
<template>
    <!-- tittle catgories -->
     <h2 class="text-3xl font-semibold 0 mb-4 ps-2 none ml-30 pt-2.5">Job Categories</h2>
  <div class="w-full max-w-(--ui-container) mx-auto z-100 top-20 sticky">
    <!-- Job Categories Wrapper -->
    <div class="w-full max-w-7xl mx-auto p-4 bg-white-300 shadow-2xl rounded-md my-6">
      <ul class="grid grid-cols-2 md:grid-cols-8 gap-4">
        <!-- Category Item -->
         <li v-for="activeLink in link" :key="activeLink">
          <NuxtLink :to="activeLink.hef"
            class="block p-4 text-center bg-gray-50 hover:bg-blue-300 shadow-xl rounded-md transition duration-300 hover:shadow-blue-400 hover:text-gray-50">
            <span class="font-medium text-gray-700">{{ activeLink.label }}</span>
          </NuxtLink>
        </li>
      </ul>
    </div>

  </div>
</template>
<script setup>
const link = [
  { label:"ALL",        hef:"/job"},
  { label:"Technology", hef:"/job/technology"},
  { label:"Accounting", hef:"/job/accounting"},
  { label:"Marketing",  hef:"/job/marketing"},
  { label:"Healthcare", hef:"/job/healthcare"},
  { label:"Design",     hef:"/job/design"},
  { label:"finance",    hef:"/job/finance"},
  { label:"sale",       hef:"/job/sale"},
]
</script>