<template>
  <div class="min-h-screen flex font-sans bg-gray-50">
    <div class="w-full md:w-1/2 bg-white flex flex-col justify-center px-8 md:px-20 py-12 overflow-y-auto">
      <div class="max-w-md mx-auto w-full">
        <div class="mb-8">
          <h1 class="text-4xl font-extrabold mb-2 bg-gradient-to-r from-indigo-600 to-blue-500 bg-clip-text text-transparent">
            CREATE ACCOUNT
          </h1>
          <p class="text-gray-400 font-medium">Join the People Solution network today.</p>
        </div>

        <form @submit.prevent="handleRegister" class="space-y-4">
          <div class="flex flex-col items-center mb-6">
            <div class="relative group cursor-pointer">
              <img
                :src="avatar || 'https://i.pravatar.cc/150'"
                class="w-24 h-24 rounded-full border-4 border-indigo-50 object-cover shadow-sm group-hover:opacity-80 transition-opacity"
              />
              <input type="file" class="absolute inset-0 w-full h-full opacity-0 cursor-pointer" @change="onAvatarChange" />
              <div class="absolute bottom-0 right-0 bg-indigo-600 text-white p-1.5 rounded-full shadow-lg">
                <i class="fa-solid fa-camera text-xs"></i>
              </div>
            </div>
            <p class="text-xs text-gray-400 mt-2 font-bold uppercase tracking-widest">Upload Photo</p>
          </div>

          <div class="grid grid-cols-1 gap-4">
            <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-3.5 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
              <i class="fa-regular fa-user text-gray-400 mr-4 group-focus-within:text-indigo-500"></i>
              <input v-model="name" type="text" placeholder="Full Name" class="w-full bg-transparent outline-none text-gray-700 font-medium" required />
            </div>

            <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-3.5 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
              <i class="fa-regular fa-envelope text-gray-400 mr-4 group-focus-within:text-indigo-500"></i>
              <input v-model="email" type="email" placeholder="Email Address" class="w-full bg-transparent outline-none text-gray-700 font-medium" required />
            </div>

            <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-3.5 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
              <i class="fa-solid fa-briefcase text-gray-400 mr-4 group-focus-within:text-indigo-500"></i>
              <input v-model="title" type="text" placeholder="Professional Title (e.g. Designer)" class="w-full bg-transparent outline-none text-gray-700 font-medium" required />
            </div>

            <div class="grid grid-cols-2 gap-4">
              <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-3.5 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
                <input v-model="company" type="text" placeholder="Company" class="w-full bg-transparent outline-none text-gray-700 font-medium" />
              </div>
              <div class="group flex items-center bg-[#f3f4ff] rounded-2xl px-5 py-3.5 transition-all focus-within:ring-2 focus-within:ring-indigo-200">
                <input v-model="expertise" type="text" placeholder="Expertise" class="w-full bg-transparent outline-none text-gray-700 font-medium" />
              </div>
            </div>
          </div>

          <button type="submit" class="w-full py-4 bg-gradient-to-r from-[#7d73ff] to-[#6358ff] hover:shadow-indigo-200 shadow-xl text-white rounded-2xl font-bold transition-all active:scale-95 hover:-translate-y-1 mt-4">
            Get Started
          </button>
        </form>

        <p class="mt-8 text-center text-gray-500 font-medium">
          Already a member? 
          <NuxtLink to="/login" class="text-indigo-600 font-bold hover:underline">Login here</NuxtLink>
        </p>
      </div>
    </div>

    <div class="hidden md:flex w-1/2 bg-[#6358ff] relative items-center justify-center overflow-hidden">
      <div class="absolute inset-0 opacity-10">
        <svg class="w-full h-full" viewBox="0 0 100 100" preserveAspectRatio="none">
          <path d="M0 100 C 20 0 50 0 100 100 Z" fill="white"></path>
        </svg>
      </div>

      <div class="relative z-10 w-[80%] max-w-md bg-white/10 backdrop-blur-2xl border border-white/20 rounded-[45px] p-12 flex flex-col text-white">
        <div class="w-16 h-1.5 bg-white rounded-full mb-6"></div>
        <h2 class="text-4xl font-bold leading-tight mb-8">
          The best opportunities are waiting for you.
        </h2>
        <div class="relative w-full h-[250px] bg-white/20 rounded-3xl overflow-hidden shadow-2xl">
          <img 
            src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&q=80&w=800" 
            class="w-full h-full object-cover" 
            alt="Teamwork"
          />
        </div>
        <p class="mt-8 text-indigo-100/80 text-lg font-medium">
          Connect with 10,000+ experts in the People Solution community.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
const user = useState('user', () => null)

const name = ref('')
const email = ref('')
const title = ref('')
const expertise = ref('')
const company = ref('')
const avatar = ref('')

const onAvatarChange = (e) => {
  const file = e.target.files[0]
  if (!file) return
  const reader = new FileReader()
  reader.onload = () => { avatar.value = reader.result }
  reader.readAsDataURL(file)
}

const handleRegister = async () => {
  const userData = {
    name: name.value,
    email: email.value,
    avatar: avatar.value,
    professional: {
      title: title.value,
      expertise: expertise.value,
      company: company.value || 'People Solution',
    }
  }

  user.value = userData
  localStorage.setItem('user', JSON.stringify(userData))
  await navigateTo('/profile')
}
</script>