<template>
  <div class="min-h-screen flex font-sans bg-gray-50">
    <div class="w-full md:w-1/2 bg-white flex flex-col justify-center px-8 md:px-20 py-12">
      <div class="max-w-md mx-auto w-full">
        <h1 class="text-4xl font-extrabold mb-2 text-center">LOGIN</h1>
        <p class="text-gray-400 text-center mb-10 font-medium">
          How to i get started lorem ipsum dolor at?
        </p>

        <form @submit.prevent="handleLogin" class="space-y-4">
          <div class="flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-4 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
            <span class="text-gray-400 mr-4"><i class="fa-regular fa-user"></i></span>
            <input type="text" placeholder="Username" class="w-full bg-transparent outline-none text-gray-700" required />
          </div>

          <div class="flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-4 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
            <span class="text-gray-400 mr-4"><i class="fa-solid fa-lock"></i></span>
            <input type="password" placeholder="Password" class="w-full bg-transparent outline-none text-gray-700" required />
          </div>

          <div class="flex justify-center pt-4">
            <button
              type="submit"
              class="cursor-pointer px-12 py-3 bg-gradient-to-r from-[#7d73ff] to-[#6358ff] hover:shadow-indigo-200 shadow-lg text-white rounded-2xl font-bold transition-transform active:scale-95"
            >
              Login Now
            </button>
          </div>

          <div class="relative flex py-8 items-center">
  <div class="flex-grow border-t border-gray-200"></div>
  
  <span class="flex-shrink mx-4 text-gray-500 text-sm font-medium">
    Or <router-link to="/register" class="text-indigo-600 font-bold hover:underline">Register Now</router-link> to 
    <span class="text-black font-bold ml-1">Login</span> with Others
  </span>
  
  <div class="flex-grow border-t border-gray-200"></div>
</div>

          <div class="space-y-3">
            <button class="w-full flex items-center justify-center gap-3 border border-gray-100 rounded-2xl py-3 hover:bg-gray-50 transition font-medium text-gray-600">
              <img src="https://www.svgrepo.com/show/475656/google-color.svg" class="w-5" />
              Login with <span class="font-bold text-black">google</span>
            </button>
            <button class="w-full flex items-center justify-center gap-3 border border-gray-100 rounded-2xl py-3 hover:bg-gray-50 transition font-medium text-gray-600">
              <img src="https://www.svgrepo.com/show/475647/facebook-color.svg" class="w-5" />
              Login with <span class="font-bold text-black">Facebook</span>
            </button>
          </div>
        </form>
      </div>
    </div>

    <div class="hidden md:flex w-1/2 bg-[#6358ff] relative items-center justify-center overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <svg class="w-full h-full" viewBox="0 0 100 100" preserveAspectRatio="none">
          <path d="M0 100 C 20 0 50 0 100 100 Z" fill="white"></path>
        </svg>
      </div>

      <div class="relative h-[500px] w-[80%] max-w-md aspect-[4/5] bg-white/10 backdrop-blur-xl border border-white/20 rounded-[45px] p-10 flex flex-col items-center">
        <h2 class="text-white text-4xl font-bold leading-tight mb-8">
          Very good works are waiting for you Login Now!!!
        </h2>
        
        <div class="relative w-full h-[300px] bg-white/20 rounded-3xl overflow-hidden shadow-lg">
          <img 
            src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?auto=format&fit=crop&q=80&w=600" 
            class="rounded-3xl shadow-2xl object-cover"
            alt="Welcome"
          />
          
          <div class="absolute ml-[30px] bottom-12 w-16 h-16 bg-white rounded-full flex items-center justify-center shadow-xl">
            <div class="bg-yellow-400 p-2 rounded-full">
               <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 20 20">
                 <path d="M11 3a1 1 0 10-2 0v1a1 1 0 102 0V3zM15.657 5.757a1 1 0 00-1.414-1.414l-.707.707a1 1 0 001.414 1.414l.707-.707zM18 10a1 1 0 01-1 1h-1a1 1 0 110-2h1a1 1 0 011 1zM5.05 6.464A1 1 0 106.464 5.05l-.707-.707a1 1 0 00-1.414 1.414l.707.707zM5 10a1 1 0 01-1 1H3a1 1 0 110-2h1a1 1 0 011 1zM8 16v-1a1 1 0 112 0v1a1 1 0 11-2 0zM13 16v-1a1 1 0 112 0v1a1 1 0 11-2 0zM14.95 14.95a1 1 0 01-1.414 0l-.707-.707a1 1 0 011.414-1.414l.707.707a1 1 0 010 1.414z" />
               </svg>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const handleLogin = () => {
  console.log("Login submitted");
};
</script>