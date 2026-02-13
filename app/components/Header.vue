<template>
  <header class="shadow-xl xl:w-[100%] xl:h-auto z-[100] t-[0] sticky p-[10px]">
    <div class="flex justify-around">
      <!-- logo -->
        
      <div class="flex items-center justify-center bg-white p-[4px]">
          <div class="flex items-center gap-1">

          <!-- PS Monogram -->
          <div class="flex items-end relative">

            <!-- P letter -->
            <div class="relative flex flex-col items-center">
              <!-- person icon on top of P -->
              <div class="mb-1 flex flex-col items-center">
                <div class="w-3 h-3 rounded-full bg-[#4a90a4] border-2 border-[#4a90a4]"></div>
                <div class="w-2 h-2 rounded-full bg-[#4a90a4] mt-0.5"></div>
              </div>
              <span class="text-6xl font-black leading-none text-[#4a7c3f]" style="font-family: Arial Black, sans-serif;">P</span>
            </div>

            <!-- S letter with circle -->
            <div class="relative -ml-1 flex flex-col items-center">
              <div class="relative">
                <!-- circle behind S -->
                <div class="absolute inset-0 flex items-center justify-center">
                  <div class="w-10 h-10 rounded-full border-4 border-[#4a90a4] opacity-80"></div>
                </div>
                <span class="relative text-6xl font-black leading-none text-[#4a7c3f] z-10" style="font-family: Arial Black, sans-serif;">S</span>
              </div>
            </div>

          </div>

            <!-- Divider line -->
            <div class="w-px h-12 bg-gray-300 mx-2"></div>

            <!-- Text: PeopleSolution -->
            <div class="flex items-center">
              <span class="text-3xl font-bold text-[#4a7c3f]" style="font-family: Arial, sans-serif;">People</span>
              <div class="flex items-end">
                <span class="text-3xl font-bold text-[#4a90a4]" style="font-family: Arial, sans-serif;">S</span>
                <span class="text-3xl font-bold text-[#4a90a4]" style="font-family: Arial, sans-serif;">olution</span>
                <!-- leaf icon -->
                <svg class="w-4 h-4 text-[#4a7c3f] mb-1 ml-0.5" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M17 8C8 10 5.9 16.17 3.82 19.34L5.71 21l1-1C8 19 9 19 12 17c3-2 4-4 4-8 0 0 2 2 2 6s-2 8-8 8c0 0 8 0 10-9 2-7-3-14-3-14z"/>
                </svg>
              </div>
            </div>
        </div>
      </div>

      <!-- lelf nav bar  -->
      <div class="blcok lg:none">
        <!-- buttons: login, signin, upload cv, anniversary -->
          <div class="flex justify-end items-center gap-4 pt-3">

            <!-- Anniversary -->
            <a href="">
              <button class="flex items-center bg-blue-500 text-white text-[15px] font-semibold px-5 py-2 rounded-full shadow-md hover:bg-blue-600 hover:shadow-blue-300 hover:shadow-lg hover:-translate-y-0.5 transition-all duration-300">
                Anniversary
              </button>
            </a>

            <!-- Upload CV -->
            <a href="">
              <button class="flex items-center bg-yellow-400 text-gray-800 text-[15px] font-semibold px-5 py-2 rounded-full shadow-md hover:bg-yellow-500 hover:shadow-yellow-300 hover:shadow-lg hover:-translate-y-0.5 transition-all duration-300">
                Upload CV
              </button>
            </a>

            <!-- Log In -->
            <a href="">
              <button class="text-[15px] font-semibold text-blue-500 border-2 border-blue-500 px-5 py-2 rounded-full hover:bg-blue-500 hover:text-white hover:-translate-y-0.5 transition-all duration-300">
                Log In
              </button>
            </a>

            <!-- Sign Up -->
            <a href="">
              <button class="text-[15px] font-semibold text-white bg-gradient-to-r from-blue-500 to-blue-700 px-5 py-2 rounded-full shadow-md hover:from-blue-600 hover:to-blue-800 hover:shadow-blue-300 hover:shadow-lg hover:-translate-y-0.5 transition-all duration-300">
                Sign Up
              </button>
            </a>

          </div>


      <!-- buttom log in sig in uploade cv and anniversary -->
        <div class="flex justify-end gap-[40px] pt-[15px]">
          <ul>
            <li class="flex gap-[30px]">

              
              <div class="relative block group">
                <a href="" class="text-[20px] font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">
                  Job Search
                </a>
                    <!-- Dropdown -->
                  <div class="absolute hidden group-hover:block top-full left-0 bg-white shadow-lg rounded-md w-[280px] z-50">
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Jobs</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Our Sectors</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full ">Register</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">My Profile</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">How To Manage My Profile</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full ">Why Apply With MyWorld Carees</a>
                  </div>
              </div>


              <div class="relative inline-block group">
                <a href="" class="text-[20px] font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">
                  Recruitment Services
                </a>
                 <!-- Dropdown -->
                  <div class="absolute hidden group-hover:block top-full left-0 bg-white shadow-lg rounded-md w-[280px] z-50 ">
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Executive Search</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Contigency Search</a>
                  </div>
              </div>


              <div class="relative inline-block group">
                <a href="" class="text-[20px] font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">
                  Outsourcing Services
                </a>
                  <!-- Dropdown -->
                  <div class="absolute hidden group-hover:block top-full left-0 bg-white shadow-lg rounded-md w-[370px] z-50">
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Prayroll Outsourcing</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Contract And Outsourcing Staffing Sulotions</a>
                  </div>
              </div>


              <div class="relative inline-block group">
                <a href="" class="text-[20px] font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">
                  About
                </a>
                  <!-- Dropdown -->
                  <div class="absolute hidden group-hover:block top-full left-0 bg-white shadow-lg rounded-md w-[280px] z-50">
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">About MyWorld Careers</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">My cooseMyWorld Careers</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Our Culture</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Meet Our LeaderShip Team</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Testimonial</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Case Studie</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">FAQ</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">SCR Activities</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">10th Anniversary</a>
                    <a href="" class="block px-4 py-2 text-[16px] hover:bg-gray-100 text-gray-700 font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">My cooseMyWorld Careers</a>
                  </div>
              </div>
          

              <a href="" class="text-[20px] font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Alog & Resourcec</a>
              <a href="" class="text-[20px] font-semibold text-gray-800 relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-[2px] after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full">Contact</a>
            </li>
          </ul>
        </div>
           
      </div>

      

    </div>   
  </header>
</template>