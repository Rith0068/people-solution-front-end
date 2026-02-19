<template>
  <header
    :class="bg-blue-300">
    <div class="max-w-350 mx-auto px-6 flex items-center justify-between gap-6">

      <NuxtLink to="/" class="flex items-center gap-2 shrink-0">
        <div class="flex items-end">
          <div class="flex flex-col items-center">
            <div class="flex flex-col items-center mb-0.5">
              <div class="w-3 h-3 rounded-full bg-[#4a90a4] border-2 border-[#4a90a4]"></div>
              <div class="w-2 h-2 rounded-full bg-[#4a90a4] mt-0.5"></div>
            </div>
            <span class="text-5xl font-black leading-none text-[#4a7c3f]"
              style="font-family: 'Arial Black', sans-serif;">P</span>
          </div>
          <div class="relative -ml-1 flex flex-col items-center">
            <div class="relative">
              <div class="absolute inset-0 flex items-center justify-center">
                <div class="w-9 h-9 rounded-full border-4 border-[#4a90a4] opacity-80"></div>
              </div>
              <span class="relative text-5xl font-black leading-none text-[#4a7c3f] z-10"
                style="font-family: 'Arial Black', sans-serif;">S</span>
            </div>
          </div>
        </div>
        <div class="w-px h-10 bg-gray-200 ml-2"></div>
        <div class="flex items-end leading-none">
          <span class="text-2xl font-bold text-[#4a7c3f]" style="font-family: Arial, sans-serif;">People</span>
          <span class="text-2xl font-bold text-[#4a90a4]" style="font-family: Arial, sans-serif;">Solution</span>
        </div>
      </NuxtLink>

      <nav class="hidden lg:flex items-center gap-7">
        <NuxtLink v-for="link in navLinks" :key="link.label" :to="link.to"
          class="relative text-[15px] font-semibold text-gray-800 pb-1 whitespace-nowrap after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-blue-500 after:transition-all after:duration-300 hover:after:w-full hover:text-blue-600 transition-colors duration-200"
          active-class="text-blue-600 after:w-full">
          {{ link.label }}
        </NuxtLink>
      </nav>

      <div class="hidden lg:flex items-center gap-3 shrink-0">

        <NuxtLink v-if="!user" to="/signup"
          class="text-[14px] font-semibold text-white bg-linear-to-r from-blue-500 to-blue-700 px-6 py-2.5 rounded-full shadow-md hover:from-blue-600 hover:to-blue-800 hover:shadow-lg transition-all duration-300">
          Sign Up Free
        </NuxtLink>

        <div v-else class="flex items-center gap-4">
          <NuxtLink to="/profile"
            class="flex items-center gap-3 bg-[#f0f7f4] hover:bg-[#e4efeb] p-1.5 pr-5 rounded-full border border-[#4a7c3f]/10 transition-all group">
            <img :src="user.avatar || 'https://i.pravatar.cc/100'"
              class="w-10 h-10 rounded-full border-2 border-white object-cover shadow-sm" />
            <div class="flex flex-col">
              <span
                class="text-[13px] font-black text-gray-900 leading-none group-hover:text-[#4a7c3f] transition-colors">
                {{ user.name }}
              </span>
              <span class="text-[10px] font-bold text-[#4a7c3f] uppercase tracking-widest mt-0.5">Account Info</span>
            </div>
          </NuxtLink>

          <button @click="logout" class="text-xs font-bold text-red-400 hover:text-red-600 underline">
            Logout
          </button>
        </div>

      </div>

      <button class="lg:hidden flex flex-col justify-center gap-1.5 p-1" @click="menuOpen = !menuOpen">
        <span :class="['block w-6 h-0.5 bg-gray-700 transition-all', menuOpen ? 'translate-y-2 rotate-45' : '']"></span>
        <span :class="['block w-6 h-0.5 bg-gray-700 transition-all', menuOpen ? 'opacity-0' : '']"></span>
        <span
          :class="['block w-6 h-0.5 bg-gray-700 transition-all', menuOpen ? '-translate-y-2 -rotate-45' : '']"></span>
      </button>
    </div>

    <div v-if="menuOpen" class="lg:hidden border-t border-gray-100 bg-white px-6 py-6 space-y-4">
      <div v-if="user" class="flex items-center gap-4 p-3 bg-gray-50 rounded-2xl">
        <img :src="user.avatar || 'https://i.pravatar.cc/100'"
          class="w-12 h-12 rounded-full border-2 border-[#4a7c3f]" />
        <div>
          <p class="font-black text-gray-900">{{ user.name }}</p>
          <NuxtLink @click="menuOpen = false" to="/profile" class="text-xs font-bold text-[#4a7c3f] underline">View
            Profile</NuxtLink>
        </div>
      </div>

      <nav class="flex flex-col gap-2">
        <NuxtLink v-for="link in navLinks" :key="link.label" :to="link.to" @click="menuOpen = false"
          class="py-2 font-bold text-gray-700 hover:text-blue-600">{{ link.label }}</NuxtLink>
      </nav>

      <div class="pt-4 border-t border-gray-50">
        <NuxtLink v-if="!user" to="/signup" @click="menuOpen = false"
          class="block text-center bg-blue-600 text-white py-3 rounded-xl font-bold">Sign Up Free</NuxtLink>
        <button v-else @click="logout"
          class="block w-full text-center bg-red-50 text-red-500 py-3 rounded-xl font-bold">Log Out</button>
      </div>
    </div>
  </header>
</template>

<script setup>
// Use global state
const user = useState('user')

// Scroll logic
const scrolled = ref(false)
const menuOpen = ref(false)

onMounted(() => {
  const onScroll = () => { scrolled.value = window.scrollY > 20 }
  window.addEventListener('scroll', onScroll, { passive: true })

  // Persist user on refresh
  const saved = localStorage.getItem('user')
  if (saved && !user.value) {
    user.value = JSON.parse(saved)
  }
})

// Logout Logic
const logout = () => {
  user.value = null
  localStorage.removeItem('user')
  menuOpen.value = false
  navigateTo('/login')
}

const navLinks = [

  { label: 'HOME', to: '/' },
  { label: 'ABOUT US', to: '/about' },
  { label: 'OUR SERVICES', to: '/services' },
  { label: 'CONTACT US', to: '/contact' },
  { label: 'JOB', to: '/job' }
]
</script>