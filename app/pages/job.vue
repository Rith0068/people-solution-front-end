<template>
  <div class="relative">
    <!-- Image -->
    <img src="../assets/images/bg-service.jpg" alt="Sample Image" class="w-full h-100 object-cover" />

    <!-- Text Overlay -->
    <div class="absolute inset-0 flex mt-2.5 items-center justify-center">
      <h1 class="text-white text-6xl font-bold p-4  bg-opacity-50">
        Find Over Hundred Job In Here
      </h1>
    </div>
  </div>

  <!-- tittle catgories -->
  <div class="w-full max-w-(--ui-container) mx-auto px-4 sm:px6 py-6">

    <!-- Job Categories Wrapper -->
    <div class="w-full max-w-7xl mx-auto p-4 bg-white shadow-2xl rounded-md my-6">
      <h2 class="text-3xl font-semibold text-gray-800 mb-4 ps-2">Job Categories</h2>

      <ul class="grid grid-cols-2 md:grid-cols-8 gap-4">
        <!-- Category Item -->
         <li>
          <a href="/job/All"
            class="block p-4 text-center bg-gray-50 hover:bg-blue-50 rounded-md border border-gray-100 transition duration-300">
            <span class="font-medium text-gray-700">All</span>
          </a>
        </li>
        
        <li>
          <a href="/job/technology"
            class="block p-4 text-center bg-gray-50 hover:bg-blue-50 rounded-md border border-gray-100 transition duration-300">
            
            <span class="font-medium text-gray-700">Technology</span>
          </a>        
        </li>

        <!-- Category Item -->
        <li>
          <a href="/job/accounting"
            class="block p-4 text-center bg-gray-50 hover:bg-blue-50 rounded-md border border-gray-100 transition duration-300">
            
            <span class="font-medium text-gray-700">Accounting</span>
          </a>
        </li>

        <!-- Category Item -->
        <li>
          <a href="/job/marketing"
            class="block p-4 text-center bg-gray-50 hover:bg-blue-50 rounded-md border border-gray-100 transition duration-300">
            
            <span class="font-medium text-gray-700">Marketing</span>
          </a>
        </li>

        <!-- Category Item -->
        <li>
          <a href="/job/healthcare"
            class="block p-4 text-center bg-gray-50 hover:bg-blue-50 rounded-md border border-gray-100 transition duration-300">
            
            <span class="font-medium text-gray-700">Healthcare</span>
          </a>
        </li>

         <!-- Category Item -->
        <li>
          <a href="/job/design"
            class="block p-4 text-center bg-gray-50 hover:bg-blue-50 rounded-md border border-gray-100 transition duration-300">
            <span class="font-medium text-gray-700">Design</span>
          </a>
        </li>


       <!-- Category Item -->
        <li>
          <a href="/job/finance"
            class="block p-4 text-center bg-gray-50 hover:bg-blue-50 rounded-md border border-gray-100 transition duration-300">
            
            <span class="font-medium text-gray-700">finance</span>
          </a>
        </li>

           <!-- Category Item -->
        <li>
          <a href="/job/sale"
            class="block p-4 text-center bg-gray-50 hover:bg-blue-50 rounded-md border border-gray-100 transition duration-300">
            
            <span class="font-medium text-gray-700">sale</span>
          </a>
        </li>
      </ul>
    </div>

  </div>

</template>
