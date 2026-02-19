<template>
  <div>

    <!-- Hero Section -->
    <div class="relative w-full h-[400px] sm:h-[500px] lg:h-[650px] overflow-hidden">
      <img src="@/assets/images/los.png" alt="" class="w-full h-full object-cover absolute inset-0">
      <div class="absolute inset-0 bg-black/40"></div>

      <div class="relative z-10 px-4 sm:px-8 lg:px-16 xl:ml-[100px] pt-12 sm:pt-20 lg:pt-[150px] max-w-7xl">
        <p class="text-yellow-500 text-[18px] sm:text-[20px] lg:text-[24px] font-semibold">
          PEO/EOR
        </p>
        <h2 class="text-gray-50 text-[28px] sm:text-[36px] lg:text-[42px] font-semibold leading-tight mt-2 sm:mt-4">
          YOUR TRUSTED LOCATION PEO <br class="hidden sm:block"> PARTNER.
        </h2>
        <p class="text-gray-50 text-[16px] sm:text-[20px] lg:text-[24px] font-semibold mt-3 sm:mt-4">
          We provide seamless, local expertise and support, ensuring your global PEO/<br class="hidden lg:block">
          Correct calculations every month.
        </p>

        <div class="flex flex-col sm:flex-row gap-4 mt-6">
          <!-- Get Started -->
          <button class="relative group overflow-hidden bg-yellow-400 text-gray-900 font-semibold w-full sm:w-[160px] h-[44px] rounded-full shadow-lg hover:shadow-xl transition-all duration-300 hover:-translate-y-0.5 active:scale-95">
            <span class="relative z-10 flex items-center justify-center gap-1.5 text-sm tracking-wide">
              Get Started
              <svg class="w-4 h-4 transition-transform duration-300 group-hover:translate-x-1" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3"/>
              </svg>
            </span>
            <div class="absolute inset-0 bg-yellow-300 translate-y-full group-hover:translate-y-0 transition-transform duration-300 rounded-full"></div>
          </button>

          <!-- Learn More -->
          <button class="relative group overflow-hidden bg-transparent text-white font-semibold w-full sm:w-[160px] h-[44px] rounded-full border-2 border-white hover:border-gray-300 transition-all duration-300 hover:-translate-y-0.5 active:scale-95">
            <span class="relative z-10 flex items-center justify-center gap-1.5 text-sm tracking-wide group-hover:text-white transition-colors duration-300">
              Learn More
            </span>
            <div class="absolute inset-0 bg-gray-800 scale-x-0 group-hover:scale-x-100 transition-transform duration-300 origin-left rounded-full"></div>
          </button>
        </div>
      </div>
    </div>

    <!-- About Section -->
    <div class="flex flex-col lg:flex-row mt-12 sm:mt-20 lg:mt-[100px] px-4 sm:px-8 lg:px-[70px] gap-8 lg:gap-12 xl:justify-around items-center w-[90%] m-auto">
      <img src="@/assets/images/tableTecnology.jpg" alt="" class="w-full sm:w-[80%] lg:w-[500px] h-auto lg:h-[270px] rounded-[10px] object-cover">

      <div class="block w-full lg:w-auto max-w-2xl">
        <RouterLink to="/about" class="bg-yellow-400 w-[90px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 transition-shadow duration-300">
          <p class="m-auto text-gray-50 py-1.5">About us</p>
        </RouterLink>

        <div class="pt-4 pb-3">
          <h2 class="font-semibold text-[20px] sm:text-[22px] lg:text-[24px] leading-tight">
            The Local HR Powerhouse Built for <br class="hidden sm:block"> Global Trust.
          </h2>
        </div>

        <p class="text-[15px] sm:text-[16px] text-gray-700 leading-relaxed">
          We are a specialized HR outsourcing and PEO agency that connects complex global needs with local expertise.
          Serving as your operational partner in Cambodia, we remove the administrative burden and legal uncertainty
          across payroll, compliance, and talent acquisition, allowing you to focus completely on strategic growth.
        </p>

        <RouterLink to="/about" class="bg-yellow-400 mt-4 sm:mt-5 w-[130px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 hover:scale-105 transition-all duration-300">
          <p class="m-auto text-gray-50 py-1.5">Explore More</p>
        </RouterLink>
      </div>
    </div>

    <div class="h-12 sm:h-16 lg:h-24"></div>

    <!-- Our Services -->
    <div class="flex px-4">
      <RouterLink to="/services" class="m-auto bg-yellow-400 w-[130px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 transition-shadow duration-300">
        <p class="m-auto text-gray-50 py-1.5 text-sm">OUR SERVICES</p>
      </RouterLink>
    </div>

    <div class="flex mt-5 px-4">
      <h2 class="m-auto font-semibold text-[20px] sm:text-[22px] lg:text-[24px]">
        Business Shaped Solutions
      </h2>
    </div>

    <!-- Service Cards -->
    <section class="py-16 w-full">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-10">

          <!-- Card 1 -->
          <div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transform transition hover:-translate-y-2 duration-300 ease-out flex flex-col">
            <div class="text-left space-y-4 flex-grow">
              <div class="w-14 h-14 flex items-center justify-center">
                <img class="w-10 h-10 object-contain" src="@/assets/images/growth.png" alt="investment">
              </div>
              <h3 class="text-lg font-semibold text-black">PEO / EOR Partnership Services</h3>
              <p class="text-gray-600 text-sm leading-relaxed">
                As your local PEO provider, we provide seamless expertise for global PEOs and EORs in Cambodia,
                ensuring your local operations are fully compliant and expertly managed.
              </p>
            </div>
            <div class="mt-6">
              <RouterLink to="/services" class="bg-yellow-400 inline-block px-6 py-2 rounded-full text-sm font-medium hover:bg-yellow-500 hover:shadow-lg transition-all duration-300">
                Read More
              </RouterLink>
            </div>
          </div>

          <!-- Card 2 -->
          <div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transform transition hover:-translate-y-2 duration-300 ease-out flex flex-col">
            <div class="text-left space-y-4 flex-grow">
              <div class="w-14 h-14 flex items-center justify-center">
                <img class="w-10 h-10 object-contain" src="@/assets/images/coin.png" alt="money">
              </div>
              <h3 class="text-lg font-semibold text-black">Payroll & National Social Security Fund (NSSF)</h3>
              <p class="text-gray-600 text-sm leading-relaxed">
                Eliminate expensive mistakes. Our payroll & NSSF calculation services provide accuracy,
                timely disbursements, and full compliance to all local tax and NSSF requirements every payroll cycle.
              </p>
            </div>
            <div class="mt-6">
              <RouterLink to="/services" class="bg-yellow-400 inline-block px-6 py-2 rounded-full text-sm font-medium hover:bg-yellow-500 hover:shadow-lg transition-all duration-300">
                Read More
              </RouterLink>
            </div>
          </div>

          <!-- Card 3 -->
          <div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transform transition hover:-translate-y-2 duration-300 ease-out flex flex-col">
            <div class="text-left space-y-4 flex-grow">
              <div class="w-14 h-14 flex items-center justify-center">
                <img class="w-10 h-10 object-contain" src="@/assets/images/check-mark.png" alt="check-mark">
              </div>
              <h3 class="text-lg font-semibold text-black">Labor Law Compliance & Registration</h3>
              <p class="text-gray-600 text-sm leading-relaxed">
                We keep your company compliant with Cambodian Labor Law and NSSF regulations.
                Need to register your company? We make the registration process simple for you.
              </p>
            </div>
            <div class="mt-6">
              <RouterLink to="/services" class="bg-yellow-400 inline-block px-6 py-2 rounded-full text-sm font-medium hover:bg-yellow-500 hover:shadow-lg transition-all duration-300">
                Read More
              </RouterLink>
            </div>
          </div>

          <!-- Card 4 -->
          <div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transform transition hover:-translate-y-2 duration-300 ease-out flex flex-col">
            <div class="text-left space-y-4 flex-grow">
              <div class="w-14 h-14 flex items-center justify-center">
                <img class="w-10 h-10 object-contain" src="@/assets/images/growth.png" alt="investment">
              </div>
              <h3 class="text-lg font-semibold text-black">Staffing and Recruitment</h3>
              <p class="text-gray-600 text-sm leading-relaxed">
                We provide strategic recruitment services to bring you the best local and foreign talent
                in the Kingdom of Cambodia.
              </p>
            </div>
            <div class="mt-6">
              <RouterLink to="/services" class="bg-yellow-400 inline-block px-6 py-2 rounded-full text-sm font-medium hover:bg-yellow-500 hover:shadow-lg transition-all duration-300">
                Read More
              </RouterLink>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- Section Image -->
    <img src="@/assets/images/smart-city.jpg" alt="" class="m-auto rounded-lg mt-[50px] w-full max-w-[1206px] h-[500px] object-cover px-4">

    <br><br>

    <!-- Why Choose Us -->
    <div class="flex flex-col lg:flex-row mt-12 sm:mt-20 lg:mt-[100px] px-4 sm:px-8 lg:px-[70px] gap-8 lg:gap-10 xl:justify-around items-center w-[90%] m-auto">

      <div class="block w-full lg:w-auto max-w-2xl">
        <RouterLink to="/about" class="bg-yellow-400 w-[130px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 transition-shadow duration-300">
          <p class="m-auto text-gray-50 py-1.5">Why Choose Us</p>
        </RouterLink>

        <div class="pt-4 pb-3">
          <h2 class="font-semibold text-[20px] sm:text-[22px] lg:text-[24px] leading-tight">
            Our Distinct Advantage
          </h2>
        </div>

        <p class="text-[15px] sm:text-[16px] text-gray-700 leading-relaxed">
          Choosing an HR or local PEO partner means selecting a guardian for your people and your compliance.
          We stand apart by offering specialized local expertise and proven experience built for global trust.
        </p>

        <div class="block divide-y divide-gray-200 mt-4">

          <!-- Accordion 1 -->
          <details class="group">
            <summary class="w-full flex items-center justify-between py-4 cursor-pointer text-base font-semibold list-none select-none transition-colors duration-200 hover:text-yellow-500">
              <span>Specialized Local Knowledge (The Expertise That Protects You)</span>
              <svg class="w-5 h-5 shrink-0 transition-transform duration-300 group-open:rotate-180" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7" />
              </svg>
            </summary>
            <div class="pb-6 pt-2 space-y-4 text-gray-700">
              <p class="text-base leading-relaxed">
                Our value begins with deep, current, and specialized knowledge of the Cambodian landscape.
                We transform complexity into certainty, ensuring your operations are flawlessly compliant.
              </p>
              <div class="space-y-3">
                <div class="pl-4 border-l-2 border-yellow-400">
                  <h6 class="text-sm font-semibold uppercase tracking-wide mb-1">Mastery of Local Laws</h6>
                  <p class="text-sm leading-relaxed">Deep expertise in Labor Laws, HR Statutes, Tax, and Employment Regulations.</p>
                </div>
                <div class="pl-4 border-l-2 border-yellow-400">
                  <h6 class="text-sm font-semibold uppercase tracking-wide mb-1">Precision Financial Compliance</h6>
                  <p class="text-sm leading-relaxed">Unwavering accuracy in Tax Codes, NSSF Contributions, and Benefits Remittance.</p>
                </div>
                <div class="pl-4 border-l-2 border-yellow-400">
                  <h6 class="text-sm font-semibold uppercase tracking-wide mb-1">Proactive Risk Mitigation</h6>
                  <p class="text-sm leading-relaxed">Constantly monitoring legislative changes to keep your policies up to date.</p>
                </div>
              </div>
            </div>
          </details>

          <!-- Accordion 2 -->
          <details class="group">
            <summary class="w-full flex items-center justify-between py-4 cursor-pointer text-base font-semibold list-none select-none transition-colors duration-200 hover:text-yellow-500">
              <span>Proven Partnership Experience (The Track Record That Defines Us)</span>
              <svg class="w-5 h-5 shrink-0 transition-transform duration-300 group-open:rotate-180" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7" />
              </svg>
            </summary>
            <div class="pb-6 pt-2 space-y-4 text-gray-700">
              <p class="text-base leading-relaxed">
                Years of successfully partnering with global PEOs and EORs has given us a proven playbook
                for seamless local execution and trusted results.
              </p>
              <div class="space-y-3">
                <div class="pl-4 border-l-2 border-yellow-400">
                  <h6 class="text-sm font-semibold uppercase tracking-wide mb-1">Global PEO Experience</h6>
                  <p class="text-sm leading-relaxed">Extensive track record working alongside leading international PEO and EOR providers.</p>
                </div>
                <div class="pl-4 border-l-2 border-yellow-400">
                  <h6 class="text-sm font-semibold uppercase tracking-wide mb-1">Trusted By Businesses</h6>
                  <p class="text-sm leading-relaxed">A growing portfolio of satisfied clients across multiple industries in Cambodia.</p>
                </div>
              </div>
            </div>
          </details>

        </div>
      </div>

      <img src="@/assets/images/tableTecnology.jpg" alt="" class="w-full sm:w-[80%] lg:w-[500px] h-auto lg:h-[400px] rounded-[10px] object-cover">

    </div>

    <br><br><br>

    <!-- Jobs & Insights -->
    <div class="flex px-4">
      <RouterLink to="/jobs" class="m-auto bg-yellow-400 w-[140px] flex rounded-[10px] shadow-xl hover:shadow-yellow-500 transition-shadow duration-300">
        <p class="m-auto text-gray-50 py-1.5 text-sm">JOB & INSIGHTS</p>
      </RouterLink>
    </div>

    <div class="flex mt-5 px-4">
      <h2 class="m-auto font-semibold text-[20px] sm:text-[22px] lg:text-[24px]">
        Latest Job Listings
      </h2>
    </div>

    <div class="flex mt-10 justify-center gap-6 flex-wrap px-4">
      <Cart />
    </div>

    <br>

    <!-- Subscribe -->
    <div class="bg-yellow-400 w-full py-16 px-6 mt-10">
      <div class="max-w-5xl mx-auto flex flex-col lg:flex-row items-center justify-between gap-8">
        <h2 class="text-[24px] sm:text-[28px] lg:text-[32px] font-semibold text-white text-center lg:text-left">
          Subscribe to get more Jobs to your inbox.
        </h2>
        <form @submit.prevent="handleSubmit" class="flex items-center gap-2 w-full max-w-md">
          <input
            type="email"
            placeholder="Enter your email address"
            class="flex-1 px-4 py-2.5 rounded-lg border border-gray-300 text-sm text-gray-800
                   placeholder-gray-400 bg-white focus:outline-none focus:ring-2
                   focus:ring-yellow-600 focus:border-transparent transition-all duration-200"
          />
          <button
            type="submit"
            class="inline-flex items-center justify-center px-5 py-2.5
                   bg-slate-800 text-white text-sm font-semibold rounded-lg shadow-md
                   hover:bg-slate-900 hover:-translate-y-0.5 active:scale-95
                   transition-all duration-200 whitespace-nowrap"
          >
            Subscribe
          </button>
        </form>
      </div>
    </div>

  </div>
</template>

<script setup>
import Cart from '~/components/Cart.vue'

const handleSubmit = (e) => {
  const email = e.target.querySelector('input[type="email"]').value
  if (email) {
    alert(`Subscribed with: ${email}`)
    e.target.reset()
  }
}
</script>

<style>
@keyframes open {
  0%   { opacity: 0; transform: translateY(-8px); }
  100% { opacity: 1; transform: translateY(0); }
}
</style>