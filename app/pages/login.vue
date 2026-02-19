<template>
  <div class="min-h-screen flex font-sans bg-gray-50">
    <div class="w-full md:w-1/2 bg-white flex flex-col justify-center px-8 md:px-20 py-12">
      <div class="max-w-md mx-auto w-full">
        <div class="mb-10 text-center md:text-left">
          <h1 class="text-4xl font-extrabold mb-2 bg-gradient-to-r from-indigo-600 to-blue-500 bg-clip-text text-transparent">
            WELCOME BACK
          </h1>
          <p class="text-gray-400 font-medium">Enter your details to access your professional dashboard.</p>
        </div>

        <form @submit.prevent="handleLogin" class="space-y-4">
          <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-4 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
            <span class="text-gray-400 mr-4 group-focus-within:text-indigo-500 transition-colors">
              <i class="fa-regular fa-envelope"></i>
            </span>
            <input 
              v-model="email" 
              type="email" 
              placeholder="Email Address" 
              class="w-full bg-transparent outline-none text-gray-700 font-medium" 
              required 
            />
          </div>

          <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-4 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
            <span class="text-gray-400 mr-4 group-focus-within:text-indigo-500 transition-colors">
              <i class="fa-solid fa-lock"></i>
            </span>
            <input 
              v-model="password" 
              type="password" 
              placeholder="Password" 
              class="w-full bg-transparent outline-none text-gray-700 font-medium" 
              required 
            />
          </div>

          <div class="flex justify-end px-2">
            <a href="#" class="text-sm text-indigo-600 font-semibold hover:underline">Forgot Password?</a>
          </div>

          <div class="pt-4">
            <button
              type="submit"
              class="w-full py-4 bg-gradient-to-r from-[#7d73ff] to-[#6358ff] hover:shadow-indigo-200 shadow-xl text-white rounded-2xl font-bold transition-all active:scale-95 hover:-translate-y-1"
            >
              Login Now
            </button>
          </div>

          <div class="relative flex py-6 items-center">
            <div class="flex-grow border-t border-gray-100"></div>
            <span class="flex-shrink mx-4 text-gray-400 text-xs font-bold uppercase tracking-widest">Or Continue With</span>
            <div class="flex-grow border-t border-gray-100"></div>
          </div>

          <div class="grid grid-cols-2 gap-4">
            <button type="button" class="flex items-center justify-center gap-2 border border-gray-100 rounded-2xl py-3 hover:bg-gray-50 transition font-bold text-gray-600">
              <img src="https://www.svgrepo.com/show/475656/google-color.svg" class="w-5" />
              Google
            </button>
            <button type="button" class="flex items-center justify-center gap-2 border border-gray-100 rounded-2xl py-3 hover:bg-gray-50 transition font-bold text-gray-600">
              <img src="https://www.svgrepo.com/show/475647/facebook-color.svg" class="w-5" />
              Facebook
            </button>
          </div>
        </form>

        <p class="mt-10 text-center text-gray-500 font-medium">
          Don't have an account? 
          <NuxtLink to="/signup" class="text-indigo-600 font-bold hover:underline">Signup Free</NuxtLink>
        </p>
      </div>
    </div>

    <div class="hidden md:flex w-1/2 bg-[#6358ff] relative items-center justify-center overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <svg class="w-full h-full" viewBox="0 0 100 100" preserveAspectRatio="none">
          <path d="M0 100 C 20 0 50 0 100 100 Z" fill="white"></path>
        </svg>
      </div>

      <div class="relative z-10 w-[80%] max-w-md bg-white/10 backdrop-blur-2xl border border-white/20 rounded-[45px] p-12 flex flex-col">
        <h2 class="text-white text-4xl font-bold leading-tight mb-8">
          Manage your projects with People Solution.
        </h2>
        
        <div class="relative w-full h-[300px] bg-white/20 rounded-3xl overflow-hidden shadow-2xl">
          <img 
            src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?auto=format&fit=crop&q=80&w=600" 
            class="w-full h-full object-cover"
            alt="Professional Workplace"
          />
        </div>

        <p class="mt-8 text-indigo-100/80 text-lg font-medium">
          Access your personalized dashboard and connect with your team.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
const user = useState('user', () => null)
const email = ref('')
const password = ref('')

const handleLogin = async () => {
  // Check if user exists in localStorage (from Signup)
  const savedUser = localStorage.getItem('user')
  
  if (savedUser) {
    const parsedUser = JSON.parse(savedUser)
    // In a real app, you would verify email/password here
    user.value = parsedUser
  } else {
    // Default fallback if no signup data found
    user.value = {
      name: "Professional User",
      email: email.value,
      professional: { title: "Executive", company: "People Solution" }
    }
  }

  // Redirect to professional profile
  await navigateTo('/profile')
}
</script>