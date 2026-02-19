<template>
  <div class="min-h-screen bg-gray-100 flex">

    <!-- SIDEBAR -->
    <aside class="w-64 bg-white border-r hidden lg:block">
      <div class="p-6 border-b flex flex-col items-center">
        <!-- Avatar Upload -->
        <div class="relative">
          <img
            :src="user.avatar || 'https://i.pravatar.cc/150'"
            class="w-20 h-20 rounded-full border object-cover"
          />
          <input
            type="file"
            class="absolute inset-0 w-full h-full opacity-0 cursor-pointer"
            @change="onAvatarChange"
          />
          <span class="absolute bottom-0 right-0 bg-indigo-600 text-white text-xs px-2 py-1 rounded-full cursor-pointer">✎</span>
        </div>

        <div class="mt-4 text-center">
          <p class="font-semibold text-gray-800">{{ user?.name }}</p>
          <p class="text-sm text-gray-500">{{ user?.email }}</p>
        </div>
      </div>

      <nav class="p-6 space-y-4 text-gray-600 font-medium">
        <p class="hover:text-indigo-600 cursor-pointer">Dashboard</p>
        <p class="hover:text-indigo-600 cursor-pointer">Messages</p>
        <p class="hover:text-indigo-600 cursor-pointer">Bookings</p>
        <p class="hover:text-indigo-600 cursor-pointer">Achievements</p>
        <p class="hover:text-indigo-600 cursor-pointer">Connections</p>
        <p class="hover:text-indigo-600 cursor-pointer">Settings</p>
      </nav>
    </aside>

    <!-- MAIN -->
    <div class="flex-1">

      <!-- HEADER -->
      <div class="bg-white px-8 py-4 flex justify-between items-center border-b">
        <h1 class="text-2xl font-bold text-gray-800">Account Settings</h1>

        <div class="flex items-center gap-6">
          <div class="relative">
            <span class="text-xl"><i class="fa-solid fa-bell"></i></span>
            <span v-if="showAlert" class="absolute -top-1 -right-2 bg-red-500 text-white text-xs px-1 rounded-full">1</span>
          </div>

          <div class="flex items-center gap-3">
            <img :src="user.avatar || 'https://i.pravatar.cc/100'" class="w-10 h-10 rounded-full object-cover" />
            <span class="font-medium">{{ user?.name }}</span>
          </div>
        </div>
      </div>

      <!-- CONTENT -->
      <div class="p-8">

        <!-- Tabs -->
        <div class="flex gap-8 border-b mb-8 text-gray-500 font-medium">
          <button @click="activeTab='profile'" :class="tabClass('profile')">Professional Profile</button>
          <button @click="activeTab='personal'" :class="tabClass('personal')">Personal Info</button>
          <button @click="activeTab='security'" :class="tabClass('security')">Security</button>
        </div>

        <div class="bg-white rounded-2xl shadow-sm divide-y">

          <!-- PROFILE -->
          <template v-if="activeTab==='profile'">
            <SettingItem label="Professional Title" v-model="form.title" />
            <SettingItem label="Expertise" v-model="form.expertise" />
            <SettingItem label="Years of Experience" v-model="form.experience" />
            <SettingItem label="Company" v-model="form.company" />
            <SettingItem label="Industry" v-model="form.industry" />
            <SettingItem label="LinkedIn" v-model="form.linkedin" />
            <SettingItem label="Portfolio Website" v-model="form.website" />
            <SettingItem label="Biography" v-model="form.bio" type="textarea" />
          </template>

          <!-- PERSONAL -->
          <template v-if="activeTab==='personal'">
            <SettingItem label="Full Name" v-model="form.name" />
            <SettingItem label="Email" v-model="form.email" />
            <SettingItem label="Phone" v-model="form.phone" />
            <SettingItem label="Location" v-model="form.location" />
            <SettingItem label="Language" v-model="form.language" />
          </template>

          <!-- SECURITY -->
          <template v-if="activeTab==='security'">
            <SettingItem label="Password" v-model="form.password" type="password" />
            <SettingItem label="Two-Factor Authentication" v-model="form.twofa" />
            <SettingItem label="Login Devices" v-model="form.devices" />
          </template>

        </div>

        <!-- Logout -->
        <div class="mt-8">
          <button @click="logout" class="bg-red-500 text-white px-6 py-3 rounded-xl font-semibold hover:bg-red-600 transition">Logout</button>
        </div>

      </div>

    </div>
  </div>
</template>

<script setup>
import SettingItem from '~/components/SettingItem.vue'

const router = useRouter()
const user = useState('user', () => null)

const activeTab = ref('profile')
const showAlert = ref(true)

onMounted(() => {
  const savedUser = localStorage.getItem('user')
  if (savedUser) user.value = JSON.parse(savedUser)
  if (!user.value) router.push('/login')
})

const form = reactive({
  title: 'Senior UI/UX Designer',
  expertise: 'Product Design, Branding, Marketing Strategy',
  experience: user.value ? Math.floor(Math.random() * 10) + 1 : '',
  company: 'Creative Studio',
  industry: 'Technology',
  linkedin: '',
  website: '',
  bio: 'Passionate designer focused on user-centered experiences and scalable digital products.',
  name: user.value?.name || '',
  email: user.value?.email || '',
  phone: '',
  location: 'United States',
  language: 'English',
  password: '',
  twofa: 'Enabled',
  devices: 'MacBook Pro, iPhone 15'
})

const logout = () => {
  user.value = null
  localStorage.removeItem('user')
  router.push('/login')
}

const tabClass = (tab) =>
  activeTab.value === tab
    ? 'border-b-2 border-indigo-600 text-indigo-600 pb-3'
    : 'pb-3 hover:text-indigo-600'

// Avatar Upload Handler
const onAvatarChange = (e) => {
  const file = e.target.files[0]
  if (!file) return
  const reader = new FileReader()
  reader.onload = () => {
    user.value.avatar = reader.result
    localStorage.setItem('user', JSON.stringify(user.value))
  }
  reader.readAsDataURL(file)
}
</script>
