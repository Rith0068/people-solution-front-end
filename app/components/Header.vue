<template>
  <header
    :class="['w-full z-[100] top-0 sticky bg-white transition-all duration-300 ease-in-out', scrolled ? 'shadow-2xl py-2' : 'shadow-xl py-3']">
    <div class="max-w-[1400px] mx-auto px-6 flex items-center justify-between gap-6">

      <!-- ── LOGO ── -->
      <NuxtLink to="/" class="flex items-center gap-2 shrink-0">

        <!-- PS Monogram -->
        <div class="flex items-end">

          <!-- P with person icon -->
          <div class="flex flex-col items-center">
            <!-- Person icon -->
            <div class="flex flex-col items-center mb-0.5">
              <div class="w-3 h-3 rounded-full bg-[#4a90a4] border-2 border-[#4a90a4]"></div>
              <div class="w-2 h-2 rounded-full bg-[#4a90a4] mt-0.5"></div>
            </div>
            <span
              class="text-5xl font-black leading-none text-[#4a7c3f]"
              style="font-family: 'Arial Black', sans-serif;"
            >P</span>
          </div>

          <!-- S with circle ring -->
          <div class="relative -ml-1 flex flex-col items-center">
            <div class="relative">
              <div class="absolute inset-0 flex items-center justify-center">
                <div class="w-9 h-9 rounded-full border-4 border-[#4a90a4] opacity-80"></div>
              </div>
              <span
                class="relative text-5xl font-black leading-none text-[#4a7c3f] z-10"
                style="font-family: 'Arial Black', sans-serif;"
              >S</span>
            </div>
          </div>
        </div>

        <!-- Divider -->
        <div class="w-px h-10 bg-gray-200"></div>

        <!-- Brand text -->
        <div class="flex items-end leading-none">
          <span
            class="text-2xl font-bold text-[#4a7c3f]"
            style="font-family: Arial, sans-serif;"
          >People</span>
          <span
            class="text-2xl font-bold text-[#4a90a4]"
            style="font-family: Arial, sans-serif;"
          >Solution</span>
          <!-- Leaf icon -->
          <svg
            class="w-4 h-4 text-[#4a7c3f] mb-1 ml-0.5 shrink-0"
            viewBox="0 0 24 24"
            fill="currentColor"
          >
            <path d="M17 8C8 10 5.9 16.17 3.82 19.34L5.71 21l1-1C8 19 9 19 12 17c3-2 4-4 4-8 0 0 2 2 2 6s-2 8-8 8c0 0 8 0 10-9 2-7-3-14-3-14z"/>
          </svg>
        </div>

      </NuxtLink>

      <!-- ── DESKTOP NAV ── -->
      <nav class="hidden lg:flex items-center gap-7">
        <NuxtLink
          v-for="link in navLinks"
          :key="link.label"
          :to="link.to"
          class="relative text-[15px] font-semibold text-gray-800 pb-1 whitespace-nowrap
                 after:absolute after:bottom-0 after:left-0
                 after:w-0 after:h-[2px] after:bg-blue-500
                 after:transition-all after:duration-300
                 hover:after:w-full hover:text-blue-600
                 transition-colors duration-200"
          active-class="text-blue-600 after:w-full"
        >
          {{ link.label }}
        </NuxtLink>
      </nav>

      <!-- ── AUTH BUTTONS (desktop) ── -->
      <div class="hidden lg:flex items-center gap-3 shrink-0">
        <NuxtLink
          to="/login"
          class="text-[14px] font-semibold text-blue-500 border-2 border-blue-500
                 px-5 py-2 rounded-full
                 hover:bg-blue-500 hover:text-white hover:-translate-y-0.5
                 transition-all duration-300"
        >
          Log In
        </NuxtLink>
        <NuxtLink
          to="/signup"
          class="text-[14px] font-semibold text-white
                 bg-gradient-to-r from-blue-500 to-blue-700
                 px-5 py-2 rounded-full shadow-md
                 hover:from-blue-600 hover:to-blue-800
                 hover:shadow-blue-300 hover:shadow-lg hover:-translate-y-0.5
                 transition-all duration-300"
        >
          Sign Up
        </NuxtLink>
      </div>

      <!-- ── HAMBURGER (mobile) ── -->
      <button
        class="lg:hidden flex flex-col justify-center gap-1.5 p-1 shrink-0"
        aria-label="Toggle navigation"
        @click="menuOpen = !menuOpen"
      >
        <span
          :class="[
            'block w-6 h-0.5 bg-gray-700 rounded transition-all duration-300',
            menuOpen ? 'translate-y-2 rotate-45' : ''
          ]"
        ></span>
        <span
          :class="[
            'block w-6 h-0.5 bg-gray-700 rounded transition-all duration-300',
            menuOpen ? 'opacity-0' : ''
          ]"
        ></span>
        <span
          :class="[
            'block w-6 h-0.5 bg-gray-700 rounded transition-all duration-300',
            menuOpen ? '-translate-y-2 -rotate-45' : ''
          ]"
        ></span>
      </button>

    </div>

    <!-- ── MOBILE MENU ── -->
    <Transition
      enter-active-class="transition-all duration-300 ease-out"
      enter-from-class="opacity-0 -translate-y-2"
      enter-to-class="opacity-100 translate-y-0"
      leave-active-class="transition-all duration-200 ease-in"
      leave-from-class="opacity-100 translate-y-0"
      leave-to-class="opacity-0 -translate-y-2"
    >
      <div v-if="menuOpen" class="lg:hidden border-t border-gray-100 bg-white">
        <nav class="flex flex-col px-6 py-3">
          <NuxtLink
            v-for="link in navLinks"
            :key="link.label"
            :to="link.to"
            class="py-3 border-b border-gray-100 text-[15px] font-semibold text-gray-700
                   hover:text-blue-600 hover:pl-2 transition-all duration-200"
            active-class="text-blue-600"
            @click="menuOpen = false"
          >
            {{ link.label }}
          </NuxtLink>

          <!-- Mobile auth buttons -->
          <div class="flex gap-3 pt-4 pb-2">
            <NuxtLink
              to="/login"
              class="flex-1 text-center text-[14px] font-semibold text-blue-500
                     border-2 border-blue-500 px-4 py-2 rounded-full
                     hover:bg-blue-500 hover:text-white transition-all duration-300"
              @click="menuOpen = false"
            >
              Log In
            </NuxtLink>
            <NuxtLink
              to="/signup"
              class="flex-1 text-center text-[14px] font-semibold text-white
                     bg-gradient-to-r from-blue-500 to-blue-700
                     px-4 py-2 rounded-full shadow-md
                     hover:from-blue-600 hover:to-blue-800 transition-all duration-300"
              @click="menuOpen = false"
            >
              Sign Up
            </NuxtLink>
          </div>
        </nav>
      </div>
    </Transition>

  </header>
</template>

<script setup>
// ── Scroll shrink ──
const scrolled = ref(false)

onMounted(() => {
  const onScroll = () => { scrolled.value = window.scrollY > 20 }
  window.addEventListener('scroll', onScroll, { passive: true })
  onUnmounted(() => window.removeEventListener('scroll', onScroll))
})

// ── Mobile menu ──
const menuOpen = ref(false)

// Close menu on route change
const route = useRoute()
watch(() => route.path, () => { menuOpen.value = false })

// ── Nav links ──
const navLinks = [
  { label: 'HOME',         to: '/'          },
  { label: 'ABOUT US',     to: '/about'     },
  { label: 'OUR SERVICES', to: '/services'  },
  { label: 'NEWS & INSIGHTS', to: '/news'   },
  { label: 'CONTACT US',   to: '/contact'   },
]
</script>