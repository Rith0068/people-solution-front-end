<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-50">
    <div class="bg-white p-10 rounded-2xl shadow-lg w-96">
      <h1 class="text-3xl font-bold mb-6 text-center">Signup</h1>

      <form @submit.prevent="handleRegister" class="space-y-4">
        <input
          v-model="name"
          type="text"
          placeholder="Full Name"
          class="w-full p-3 border rounded-lg"
          required
        />

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
          Register
        </button>
      </form>

      <p class="mt-4 text-center">
        Already have account?
        <NuxtLink to="/login" class="text-indigo-600 font-bold">
          Login
        </NuxtLink>
      </p>
    </div>
  </div>
</template>

<script setup>
const router = useRouter()
const user = useState('user', () => null)

const name = ref('')
const email = ref('')
const password = ref('')

const handleRegister = () => {
  const userData = {
    name: name.value,
    email: email.value
  }

  user.value = userData
  localStorage.setItem('user', JSON.stringify(userData))

  router.push('/profile')
}
</script>
