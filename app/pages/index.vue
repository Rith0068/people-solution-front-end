<template>
    <!-- hero section -->
    <div class="relative w-full h-[400px] sm:h-[500px] lg:h-[650px] overflow-hidden">
        <img src="@/assets/images/los.png" alt="" class="w-full h-full object-cover blur-[0.1px] absolute inset-0">
        
        <div class="relative z-10 px-4 sm:px-8 lg:px-16 xl:ml-[100px] pt-12 sm:pt-20 lg:pt-[150px] max-w-7xl">
            <div class="text-start">
                <p class="text-gray-50 text-[18px] sm:text-[20px] lg:text-[24px] font-semibold text-yellow-500">
                    PEO/EOR
                </p>
            </div>
            <div class="text-start mt-2 sm:mt-4">
                <h2 class="text-gray-50 text-[28px] sm:text-[36px] lg:text-[42px] font-semibold leading-tight">
                    YOUR TRUSTED LOCATION PEO
                    <br class="hidden sm:block">PARTNER.
                </h2>
            </div>
            <div class="text-start mt-3 sm:mt-4">
                <p class="text-gray-50 text-[16px] sm:text-[20px] lg:text-[24px] font-semibold">
                    we provid seamless, local expertise and support,ensuring you global PEO/
                    <br class="hidden lg:block">Correct calculations every month.
                </p>
            </div>
            <div class="flex flex-col sm:flex-row gap-4 sm:gap-[20px] mt-6 sm:mt-[10px]">
                <!-- Get Started Button -->
                <button class="relative group overflow-hidden bg-yellow-400 text-gray-900 font-semibold w-full sm:w-[160px] h-[44px] rounded-full shadow-lg shadow-yellow-300/40 hover:shadow-yellow-400/60 hover:shadow-xl transition-all duration-300 hover:-translate-y-0.5 active:translate-y-0 active:scale-95">
                    <span class="relative z-10 flex items-center justify-center gap-1.5 text-sm tracking-wide">
                        Get Started
                        <svg class="w-4 h-4 transition-transform duration-300 group-hover:translate-x-1" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3"/>
                        </svg>
                    </span>
                    <div class="absolute inset-0 bg-yellow-300 translate-y-full group-hover:translate-y-0 transition-transform duration-300 rounded-full"></div>
                </button>

                <!-- Learn More Button -->
                <button class="relative group overflow-hidden bg-gray-500 text-gray-700 font-semibold w-full sm:w-[160px] h-[44px] rounded-full border-2 border-gray-300 hover:border-gray-700 transition-all duration-300 hover:-translate-y-0.5 active:translate-y-0 active:scale-95">
                    <span class="relative z-10 flex items-center justify-center gap-1.5 text-sm tracking-wide group-hover:text-white transition-colors duration-300">
                        Learn More
                    </span>
                    <div class="absolute inset-0 bg-gray-800 scale-x-0 group-hover:scale-x-100 transition-transform duration-300 origin-left rounded-full"></div>
                </button>
            </div>
        </div>
    </div>
    <!-- ending hero section -->

    <!-- About Section -->
    <div class="flex flex-col lg:flex-row mt-12 sm:mt-20 lg:mt-[100px] px-4 sm:px-8 lg:px-[70px] gap-8 lg:gap-12 xl:justify-around items-center lg:items-start w-[90%] m-auto">
        <img src="@/assets/images/tableTecnology.jpg" alt="" class="w-full sm:w-[80%] lg:w-[500px] h-auto lg:h-[270px] rounded-[10px] object-cover">
        
        <div class="block w-full lg:w-auto max-w-2xl">
            <RouterLink to="about" class="bg-yellow-400 w-[90px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 transition-shadow duration-300">
                <p class="m-auto text-gray-50 py-1.5">
                    About us
                </p>
            </RouterLink>

            <div class="pt-4 pb-3">
                <h2 class="font-semibold text-[20px] sm:text-[22px] lg:text-[24px] leading-tight">
                    The Local HR Powerhouse Built for 
                    <br class="hidden sm:block">Global Trust.
                </h2>
            </div>
            
            <div class="block">
                <p class="text-[15px] sm:text-[16px] text-gray-700 leading-relaxed">
                    We are a specialized HR outsourcing and PEO agency that connects
                    complex global needs with local expertise. Serving as your 
                    operational partner in Cambodia, we remove the administrative 
                    burden and legal uncertainty across payroll, compliance, and talent 
                    acquisition, allowing you to focus completely on strategic growth.  
                </p>
            </div>
            
            <RouterLink to="about" class="bg-yellow-400 mt-4 sm:mt-5 w-[130px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 hover:scale-105 transition-all duration-300 inline-flex">
                <p class="m-auto text-gray-50 py-1.5">
                    Explore More
                </p>
            </RouterLink>
        </div>
    </div>

    <div class="h-12 sm:h-16 lg:h-24"></div>

    <!-- our short service -->
    <div class="flex px-4">
        <RouterLink to="about" class="m-auto bg-yellow-400 w-[130px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 transition-shadow duration-300">
            <p class="m-auto text-gray-50 py-1.5 text-sm sm:text-base">
                OUR SERVICES
            </p>
        </RouterLink>
    </div>
    
    <br>
    <!-- Business Shaped Solutions -->
    <div class="flex mt-5 sm:mt-6 lg:mt-[20px] px-4">
        <h2 class="m-auto font-semibold text-[20px] sm:text-[22px] lg:text-[24px] leading-tight">
            Business Shaped Solutions
        </h2>
    </div>

        <!-- service card section -->
    <section class="py-30 slide-up-animation animate-in data-scroll-section w-full">
        <div class="max-w-7xl m-auto px-4 sm:px-6 lg:px-8">
            <!-- each card -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
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
                <div class="mt-auto pt-6">
                <a class="bg-[rgb(233,219,105)] inline-block px-6 py-2 rounded-full font-md transition-duration-300 ease-out hover-scale-105 hover:shadow-yellow-lg text-sm"
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
                    <img class="-10 h-10 fill-nonestrock-currentColor" src="../assets/image/growth.png" alt="investment">
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
        <!-- sechtion img -->
        <img src="@/assets/images/smart-city.jpg" alt="" class="m-auto rounded-lg mt-[50px] w-[1206px] h-[500px]">

        <br><br>


        <!-- About Section -->
        <div class="flex flex-col lg:flex-row mt-12 sm:mt-20 lg:mt-[100px] px-4 sm:px-8 lg:px-[70px] gap-8 lg:gap-10 xl:justify-around items-center lg:items-start w-[90%] m-auto">


            <div class="block w-full lg:w-auto max-w-2xl ml-[0px]">
                <RouterLink to="about" class="bg-yellow-400 w-[130px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 transition-shadow duration-300">
                    <p class="m-auto text-gray-50 py-1.5">
                       Why Choose Us
                    </p>
                </RouterLink>
                
                <div class="pt-4 pb-3">
                    <h2 class="font-semibold text-[20px] sm:text-[22px] lg:text-[24px] leading-tight">
                        Our Distinct Advantage
                    </h2>
                </div>
                
                <div class="block">
                    <p class="text-[15px] sm:text-[16px] text-gray-700 leading-relaxed">
                        Choosing an HR or local PEO partner means selecting a guardian for 
                        your people and your compliance. We stand apart by offering 
                        specialized local expertise and proven experience built for global  
                        trust.  
                    </p>
                </div>
                <div class="block divide-y divide-black">

    <!-- Accordion Item 1 -->
    <details class="group">
      <summary
        class="w-full flex items-center justify-between py-4 cursor-pointer text-xl font-light list-none select-none
               transition-colors duration-200 hover:text-gray-500"
      >
        <span>Specialized Local Knowledge (The Expertise That Protects You)</span>
        <!-- Chevron icon -->
        <svg
          class="w-5 h-5 shrink-0 transition-transform duration-300 group-open:rotate-180"
          xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"
        >
          <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7" />
        </svg>
      </summary>

      <div class="overflow-hidden animate-[open_0.3s_ease] pb-6 pt-2 space-y-4 text-gray-700">
        <p class="text-base leading-relaxed">
          Our value begins with deep, current, and specialized knowledge of the Cambodian landscape.
          We transform complexity into certainty, ensuring your operations are flawlessly compliant.
        </p>
        <div class="space-y-3">
          <div class="pl-4 border-l-2 border-black">
            <h6 class="text-sm font-semibold text-black uppercase tracking-wide mb-1">Mastery of Local Laws</h6>
            <p class="text-sm leading-relaxed">
              Deep, current expertise in all local Labor Laws, HR Statutes, Tax, and Employment Regulations,
              turning legal ambiguity into operational certainty.
            </p>
          </div>
          <div class="pl-4 border-l-2 border-black">
            <h6 class="text-sm font-semibold text-black uppercase tracking-wide mb-1">Precision Financial Compliance</h6>
            <p class="text-sm leading-relaxed">
              Unwavering accuracy in navigating Tax Codes, National Social Security Fund Contributions,
              and Benefits Remittance, guaranteeing audit-ready and timely payroll.
            </p>
          </div>
          <div class="pl-4 border-l-2 border-black">
            <h6 class="text-sm font-semibold text-black uppercase tracking-wide mb-1">Proactive Risk Mitigation</h6>
            <p class="text-sm leading-relaxed">
              Our experts are constantly monitoring legislative changes, allowing us to proactively
              update your policies and eliminate exposure to fines or legal action.
            </p>
          </div>
        </div>
      </div>
    </details>

    <!-- Accordion Item 2 -->
    <details class="group">
      <summary
        class="w-full flex items-center justify-between py-4 cursor-pointer text-xl font-light list-none select-none
               transition-colors duration-200 hover:text-gray-500"
      >
            <span>Proven Partnership Experience (The Track Record That Defines Us)</span>
            <svg
            class="w-5 h-5 shrink-0 transition-transform duration-300 group-open:rotate-180"
            xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"
            >
            <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7" />
            </svg>
        </summary>

        <div class="overflow-hidden animate-[open_0.3s_ease] pb-6 pt-2 space-y-4 text-gray-700">
            <p class="text-base leading-relaxed">
            Our value begins with deep, current, and specialized knowledge of the Cambodian landscape.
            We transform complexity into certainty, ensuring your operations are flawlessly compliant.
            </p>
            <div class="space-y-3">
            <div class="pl-4 border-l-2 border-black">
                <h6 class="text-sm font-semibold text-black uppercase tracking-wide mb-1">Mastery of Local Laws</h6>
                <p class="text-sm leading-relaxed">
                Deep, current expertise in all local Labor Laws, HR Statutes, Tax, and Employment Regulations,
                turning legal ambiguity into operational certainty.
                </p>
            </div>
            <div class="pl-4 border-l-2 border-black">
                <h6 class="text-sm font-semibold text-black uppercase tracking-wide mb-1">Precision Financial Compliance</h6>
                <p class="text-sm leading-relaxed">
                Unwavering accuracy in navigating Tax Codes, National Social Security Fund Contributions,
                and Benefits Remittance, guaranteeing audit-ready and timely payroll.
                </p>
            </div>
            <div class="pl-4 border-l-2 border-black">
                <h6 class="text-sm font-semibold text-black uppercase tracking-wide mb-1">Proactive Risk Mitigation</h6>
                <p class="text-sm leading-relaxed">
                Our experts are constantly monitoring legislative changes, allowing us to proactively
                update your policies and eliminate exposure to fines or legal action.
                </p>
            </div>
            </div>
        </div>
        </details>

        </div>
            </div>

            <img src="@/assets/images/tableTecnology.jpg" alt="" class="w-full sm:w-[80%] lg:w-[500px] h-[auto] lg:h-[270px] rounded-[10px] object-cover ">

        </div>  

        <br><br><br>
        <!-- NEWS & INSIGHTS -->
        <RouterLink to="about" class="bg-yellow-400 w-[130px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 transition-shadow duration-300 m-auto">
            <p class="m-auto text-gray-50 py-1.5">
                JOB & INSIGHTS
            </p>
        </RouterLink>    
        <br>
        <!-- Business Shaped Solutions -->
        <div class="flex mt-5 sm:mt-6 lg:mt-[20px] px-4">
            <h2 class="m-auto font-semibold text-[20px] sm:text-[22px] lg:text-[24px] leading-tight">
                Business Shaped Solutions
            </h2>
        </div>

        <div class="flex mt-[100px] justify-center gap-[210px]">
            <Cart />
        </div>
        <br>
        <!-- Subscribe -->
        <div class="bg-yellow-500 w-[100%] h-[300px] flex">
            <div class="flex m-auto gap-[300px]">
                <h2 class="text-[32px] font-semibold">
                    Subscribe to get more Jobs to your inbox. 
                </h2>
                <form
                    @submit.prevent="handleSubmit"
                    class="flex items-center gap-2 w-full max-w-md"
                >
                    <input
                    type="email"
                    placeholder="Enter your email address"
                    class="flex-1 px-4 py-2.5 rounded-lg border border-gray-300 text-sm
                            text-gray-800 placeholder-gray-400 bg-white
                            focus:outline-none focus:ring-2 focus:ring-yellow-400 focus:border-transparent
                            transition-all duration-200"
                    />

                    <button
                    type="submit"   
                    class="inline-flex items-center justify-center px-5 py-2.5
                            bg-yellow-400 text-white text-sm font-semibold rounded-lg
                            shadow-md hover:bg-yellow-500 hover:shadow-yellow-400/50
                            hover:-translate-y-0.5 active:scale-95
                            transition-all duration-200 whitespace-nowrap"
                    >
                    Subscribe
                    </button>
                </form>
            </div>
        </div>
</template>
<script setup>
import Cart from '~/components/Cart.vue';
</script>
<style>
@keyframes open {
  0%   { opacity: 0; }
  100% { opacity: 1; }
}
</style>