<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-100">
    <div class="w-full max-w-4xl bg-white rounded-xl shadow-lg overflow-hidden flex">

      <!-- Left side (Welcome/Register) -->
      <div class="w-1/2 bg-blue-400 text-white p-12 flex flex-col justify-center items-center">
        <h1 class="text-3xl font-bold mb-4">
          {{ isLogin ? 'Hello, Welcome!' : 'Join Us!' }}
        </h1>
        <p class="mb-6 text-center">
          {{ isLogin ? "Don't have an account?" : "Already have an account?" }}
        </p>
        <button
          @click="toggleForm"
          class="border border-white px-6 py-2 rounded hover:bg-white hover:text-blue-400 transition"
        >
          {{ isLogin ? 'Register' : 'Login' }}
        </button>
      </div>

      <!-- Right side (Form) -->
      <div class="w-1/2 p-12 flex flex-col justify-center">
        <h2 class="text-2xl font-bold mb-6 text-gray-700">
          {{ isLogin ? 'Login' : 'Register' }}
        </h2>

        <form @submit.prevent="handleSubmit" class="space-y-4">

          <!-- Username / Email -->
          <input
            v-model="form.username"
            type="text"
            placeholder="Username"
            class="w-full px-4 py-3 rounded border border-gray-300 focus:ring-2 focus:ring-blue-400 outline-none"
            required
          />

          <!-- Password -->
          <input
            v-model="form.password"
            type="password"
            placeholder="Password"
            class="w-full px-4 py-3 rounded border border-gray-300 focus:ring-2 focus:ring-blue-400 outline-none"
            required
          />

          <!-- Confirm Password (only for register) -->
          <input
            v-if="!isLogin"
            v-model="form.confirmPassword"
            type="password"
            placeholder="Confirm Password"
            class="w-full px-4 py-3 rounded border border-gray-300 focus:ring-2 focus:ring-blue-400 outline-none"
            required
          />

          <!-- Error message -->
          <p v-if="errorMessage" class="text-red-500 text-sm">
            {{ errorMessage }}
          </p>

          <!-- Submit button -->
          <button
            type="submit"
            class="w-full bg-blue-400 text-white py-3 rounded font-bold hover:bg-blue-500 transition"
          >
            {{ isLogin ? 'Login' : 'Register' }}
          </button>
        </form>

        <!-- Social login -->
        <p class="mt-6 text-center text-gray-500 text-sm">
          or login with social platforms
        </p>
        <div class="flex justify-center gap-4 mt-2">
          <!-- Google -->
          <button class="border rounded px-3 py-2 hover:bg-gray-100 transition">
            <i class="fa-brands fa-google text-red-500 text-xl"></i>
          </button>

          <!-- Facebook -->
          <button class="border rounded px-3 py-2 hover:bg-gray-100 transition">
            <i class="fa-brands fa-facebook-f text-blue-600 text-xl"></i>
          </button>

          <!-- GitHub -->
          <button class="border rounded px-3 py-2 hover:bg-gray-100 transition">
            <i class="fa-brands fa-github text-gray-800 text-xl"></i>
          </button>

          <!-- LinkedIn -->
          <button class="border rounded px-3 py-2 hover:bg-gray-100 transition">
            <i class="fa-brands fa-linkedin-in text-blue-700 text-xl"></i>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const isLogin = ref(true) // true = login form, false = register form

const form = ref({
  username: '',
  password: '',
  confirmPassword: ''
})

const errorMessage = ref('')

// Toggle between login and register
const toggleForm = () => {
  isLogin.value = !isLogin.value
  errorMessage.value = ''
  form.value.username = ''
  form.value.password = ''
  form.value.confirmPassword = ''
}

// Submit form
const handleSubmit = () => {
  errorMessage.value = ''

  if (!isLogin.value && form.value.password !== form.value.confirmPassword) {
    errorMessage.value = "Passwords do not match"
    return
  }

  if (isLogin.value) {
    console.log("Login:", form.value)
    // Call login API here
  } else {
    console.log("Register:", form.value)
    // Call register API here
  }
}
</script>