<template>
  <!-- hero section service -->
  <div class="relative">
    <!-- Image -->
    <img src="../assets/images/job-requirment.jpg" alt="Sample Image" class="w-full h-100  object-cover" />

    <!-- Text Overlay -->
    <div class="absolute inset-0 mx-aotu mt-30 items-center justify-center">
      <h1 class="text-white text-center text-4xl md:text-4xl font-bold p-4 bg-opacity-50">
        Find Thousand Jobs If You're Ready To Get
      </h1>

      <!-- input sreach job -->
      <!-- Wrapper to center the input -->
      <div class="flex justify-center w-full">
        <form action="/action_page.php">
          <select class="border border-gray-300 rounded-lg px-4 py-4 font-bold text-2xl w-md focus:outline-none focus:ring-2 focus-[#E9C46A] text-white" name="job" id="job">
            <option value="volvo">Find your job here ...</option>
            <option value="saab">Wen development</option>
            <option value="opel">Accounting</option>
            <option value="audi">Marketing</option>
            <option value="audi">Design</option>
            <option value="audi">Medical/Nurse/Health</option>
            <option value="audi">Finance</option>
          </select>
        </form>
      </div>
    </div>
  </div>

 
</template>