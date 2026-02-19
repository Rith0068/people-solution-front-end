<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-50">
    <div class="bg-white p-10 rounded-2xl shadow-lg w-96">
      <h1 class="text-3xl font-bold mb-6 text-center">Login</h1>

      <form @submit.prevent="handleLogin" class="space-y-4">
        <input
          v-model="email"
          type="email"
          placeholder="Email"
          class="w-full p-3 border rounded-lg"
          required
        />

        <input
          v-model="password"
          type="password"
          placeholder="Password"
          class="w-full p-3 border rounded-lg"
          required
        />

        <button
          type="submit"
          class="w-full bg-indigo-600 text-white p-3 rounded-lg font-bold"
        >
          Login
        </button>
      </form>

      <p class="mt-4 text-center">
        Don't have account?
        <NuxtLink to="/signup" class="text-indigo-600 font-bold">
          Signup
        </NuxtLink>
      </p>
    </div>
  </div>
</template>

<script setup>
const router = useRouter()
const user = useState('user', () => null)

const email = ref('')
const password = ref('')

onMounted(() => {
  const savedUser = localStorage.getItem('user')
  if (savedUser) {
    user.value = JSON.parse(savedUser)
  }
})

const handleLogin = () => {
  const userData = {
    name: "User",
    email: email.value
  }

  user.value = userData
  localStorage.setItem('user', JSON.stringify(userData))

  router.push('/profile')
}
</script>
