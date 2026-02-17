<template>
  <div class="bg-gray-100">
    <!-- hero section service -->
    <div class="relative">
      <!-- Image -->
      <img src="../assets/image/bg-service.jpg" alt="Sample Image" class="w-full h-100 object-cover" />

      <!-- Text Overlay -->
      <div class="absolute inset-0 flex mt-2.5 items-center justify-center">
        <h1 class="text-white text-6xl font-bold p-4  bg-opacity-50">
          OUR SERVICE
        </h1>
      </div>
    </div>


    <!-- Our Story Section -->
    <section class="bg-gray py-20">
      <div class="max-w-7xl mx-auto px-6">

        <div class="grid md:grid-cols-2 gap-12 items-start">

          <!-- Left Content -->
          <div>

            <!-- Badge -->
            <span class="inline-block bg-yellow-400 text-slate-800 text-sm font-semibold px-4 py-1 rounded-full mb-6">
              OUR SERVICE
            </span>

            <!-- Title -->
            <h2 class="text-4xl md:text-5xl font-bold text-slate-800 leading-tight">
              Premium HR Services Tailored for Cambodia.
            </h2>

          </div>

          <!-- Right Content -->
          <div>
            <p class="text-slate-600 text-lg leading-relaxed">
              We deliver expert recruitment, payroll, and HR solutions—helping your business grow with trusted support
              and
              local
              expertise. Our comprehensive approach ensures seamless integration of HR best practices tailored
              specifically
              for
              the Cambodian market.
            </p>
          </div>

        </div>
      </div>
    </section>



    <!-- service card section -->
    <section class="py-30 slide-up-animation animate-in data-scroll-section w-full">
      <div class="max-w-7xl m-auto px-4 sm:px-6 lg:px-8">
        <!-- each card -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div
            class="bg-white-500 rounded-2xl p-8 shadow-lg hover:shadow-lg transform transition hover:-translate-y-4 hover:scale-110duration-300 ease-out ">
            <div class="text-left space-y-4 fles-grow">
              <div class="w-14 h-14 flex items-center justify-center">
                <img class="-10 h-10 fill-none strock-currentColor" src="../assets/image/growth.png" alt="investment">
              </div>
              <h3 class="text-lg font-semibold text-black">PEO / EOR Partnership Services</h3>
              <p class="text-gray-600 text-sm leading-relaxed">As your local PEO provider, we provide seamless expertise
                for
                global PEOs and EORs in Cambodia, ensuring your local operations are fully compliant and expertly
                managed.
              </p>
            </div>
            <div class="mt-auto pt-6 ">
              <a class="bg-[rgb(233,219,105)] inline-block px-6 py-2 rounded-full font-md transition-duration-300 ease-out hover-scale-105 hover:shadow-lg text-sm"
                href="">
                Read More
              </a>
            </div>
          </div>

          <div
            class="bg-white-500 rounded-2xl p-8 shadow-lg hover:shadow-lg transform transition hover:-translate-y-4 hover:scale-110duration-300 ease-out ">
            <div class="text-left space-y-4 fles-grow">
              <div class="w-14 h-14 flex items-center justify-center">
                <img class="-10 h-10 fill-none strock-currentColor" src="../assets/image/coin.png" alt="money">
              </div>
              <h3 class="text-lg font-semibold text-black">Payroll & National Social Security Fund (NSSF)</h3>
              <p class="text-gray-600 text-sm leading-relaxed">AEliminate expensive mistakes. Our payroll & NSSF
                calculation services provide accuracy, timely disbursements, and full compliance to all local tax and
                NSSF requirements every payroll cycle.
              </p>
            </div>
            <div class="mt-auto pt-6 ">
              <a class="bg-[rgb(233,219,105)] inline-block px-6 py-2 rounded-full font-md transition-duration-300 ease-out hover-scale-105 hover:shadow-lg text-sm"
                href="">
                Read More
              </a>
            </div>
          </div>

          <div
            class="bg-white-500 rounded-2xl p-8 shadow-lg hover:shadow-lg transform transition hover:-translate-y-4 hover:scale-110duration-300 ease-out  ">
            <div class="text-left space-y-4 fles-grow">
              <div class="w-14 h-14 flex items-center justify-center">
                <img class="-10 h-10 fill-none strock-currentColor" src="../assets/image/check-mark.png"
                  alt="check-mark.png">
              </div>
              <h3 class="text-lg font-semibold text-black">Labor Law Compliance & Registration</h3>
              <p class="text-gray-600 text-sm leading-relaxed">We keep your company compliant with Cambodian Labor Law
                and NSSF regulations. Need to register your company? We make the registration process simple for you.
              </p>
            </div>
            <div class="mt-auto pt-6 ">
              <a class="bg-[rgb(233,219,105)] inline-block px-6 py-2 rounded-full font-md transition-duration-300 ease-out hover-scale-105 hover:shadow-lg text-sm"
                href="">
                Read More
              </a>
            </div>
          </div>

          <div
            class="bg-white-500 rounded-2xl p-8 shadow-lg hover:shadow-lg transform transition hover:-translate-y-4 hover:scale-110duration-300 ease-out  ">
            <div class="text-left space-y-4 fles-grow">
              <div class="w-14 h-14 flex items-center justify-center">
                <img class="-10 h-10 fill-none strock-currentColor" src="../assets/image/growth.png" alt="investment">
              </div>
              <h3 class="text-lg font-semibold text-black">Staffing and Recruitment</h3>
              <p class="text-gray-600 text-sm leading-relaxed">We provide strategic recruitment services to bring you
                the best local and foreign talent in the Kingdom of Cambodia.
              </p>
            </div>
            <div class="mt-auto pt-6 ">
              <a class="bg-[rgb(233,219,105)] inline-block px-6 py-2 rounded-full font-md transition-duration-300 ease-out hover-scale-105 hover:shadow-lg text-sm"
                href="">
                Read More
              </a>
            </div>
          </div>

        </div>
      </div>

    </section>

    <div class="fixed bottom-8 right-8">
      <button @click="scrollToTop"
        class="bg-[#E9C46A] w-12 h-12 rounded-lg flex items-center justify-center shadow-lg hover:-translate-y-1 transition-transform">
        <i class="fa-solid fa-arrow-up text-[#2D3E50]"></i>
      </button>
    </div>

  </div>


</template>
<script setup>
const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};
</script>