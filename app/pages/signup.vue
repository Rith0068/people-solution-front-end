<template>
  <div class="min-h-screen flex font-sans bg-gray-50">
    
    <div class="w-full md:w-1/2 bg-white flex flex-col justify-center px-8 md:px-20 py-12">
      <div class="max-w-md mx-auto w-full">
        <div class="mb-10">
          <h1 class="text-4xl font-extrabold mb-2 bg-gradient-to-r from-indigo-600 to-blue-500 bg-clip-text text-transparent">
            CREATE ACCOUNT
          </h1>
          <p class="text-gray-400 font-medium">Join us and start your journey today.</p>
        </div>

        <form @submit.prevent="handleRegister" class="space-y-4">
          <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-4 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
            <span class="text-gray-400 mr-4 group-focus-within:text-indigo-500 transition-colors">
              <i class="fa-regular fa-id-card"></i>
            </span>
            <input type="text" placeholder="Full Name" class="w-full bg-transparent outline-none text-gray-700" required />
          </div>

          <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-4 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
            <span class="text-gray-400 mr-4 group-focus-within:text-indigo-500 transition-colors">
              <i class="fa-regular fa-envelope"></i>
            </span>
            <input type="email" placeholder="Email Address" class="w-full bg-transparent outline-none text-gray-700" required />
          </div>

          <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-4 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
            <span class="text-gray-400 mr-4 group-focus-within:text-indigo-500 transition-colors">
              <i class="fa-solid fa-lock"></i>
            </span>
            <input type="password" placeholder="Create Password" class="w-full bg-transparent outline-none text-gray-700" required />
          </div>

          <div class="flex items-center px-2">
            <input type="checkbox" id="terms" class="w-4 h-4 text-indigo-600 border-gray-300 rounded focus:ring-indigo-500" required>
            <label for="terms" class="ml-2 text-sm text-gray-500">
              I agree to the <a href="#" class="text-indigo-600 hover:underline">Terms & Conditions</a>
            </label>
          </div>

          <div class="flex flex-col items-center pt-4">
            <button
              type="submit"
              class="w-full md:w-auto px-16 py-4 bg-gradient-to-r from-[#7d73ff] to-[#6358ff] hover:shadow-indigo-200 shadow-xl text-white rounded-2xl font-bold transition-all active:scale-95 hover:-translate-y-1"
            >
              Get Started
            </button>
            
            <p class="mt-8 text-gray-500">
              Already a member? 
              <router-link to="/login" class="text-indigo-600 font-bold hover:underline">Login here</router-link>
            </p>
          </div>
        </form>
      </div>
    </div>

    <div class="hidden md:flex w-1/2 bg-[#6358ff] relative items-center justify-center overflow-hidden">
      <div class="absolute top-0 -left-20 w-72 h-72 bg-white/10 rounded-full blur-3xl"></div>
      <div class="absolute bottom-0 -right-20 w-96 h-96 bg-blue-400/20 rounded-full blur-3xl"></div>

      <div class="relative z-10 w-[80%] max-w-md bg-white/10 backdrop-blur-2xl border border-white/20 rounded-[45px] p-12 flex flex-col">
        <div class="mb-8">
           <div class="w-16 h-1 w-12 bg-white rounded-full mb-4"></div>
           <h2 class="text-white text-4xl font-bold leading-tight">
             Adventure starts with a single click.
           </h2>
        </div>
        
        <div class="relative h-[250px] w-full rounded-3xl overflow-hidden group">
          <img 
            src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&q=80&w=800" 
            class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
            alt="Teamwork"
          />
          <div class="absolute left-6 top-1/2 -translate-y-1/2 w-14 h-14 bg-white rounded-2xl flex items-center justify-center shadow-2xl rotate-12 group-hover:rotate-0 transition-transform">
            <svg class="w-8 h-8 text-indigo-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6" />
            </svg>
          </div>
        </div>

        <p class="mt-8 text-indigo-100/80 text-lg">
          Connect with over 10,000+ creators and professionals worldwide.
        </p>
      </div>
    </div>

  </div>
</template>

<script setup>
const handleRegister = () => {
  alert("Registration Successful! (Check Console)");
  console.log("Registration logic goes here...");
};
</script>