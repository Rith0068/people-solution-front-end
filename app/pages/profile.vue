<template>
  <div class="min-h-screen bg-[#f8fafc] font-sans">
    <main class="max-w-[1200px] mx-auto pt-10 px-6 pb-20">
      
      <div class="bg-white rounded-[32px] p-8 shadow-sm border border-gray-100 flex flex-col md:flex-row items-center gap-8 mb-10">
        <div class="relative group">
          <div class="w-32 h-32 rounded-full border-4 border-[#f0f7f4] overflow-hidden shadow-md">
            <img 
              src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?auto=format&fit=crop&q=80&w=200" 
              alt="User Avatar"
              class="w-full h-full object-cover"
            />
          </div>
          <button class="absolute bottom-1 right-1 bg-[#4a7c3f] text-white p-2 rounded-full shadow-lg hover:scale-110 transition-transform">
            <i class="fa-solid fa-camera text-xs"></i>
          </button>
        </div>

        <div class="flex-grow text-center md:text-left">
          <div class="flex flex-col md:flex-row md:items-center gap-3 mb-2">
            <h1 class="text-3xl font-black text-gray-900 tracking-tight">John Doe</h1>
            <span class="bg-[#4a7c3f]/10 text-[#4a7c3f] text-xs font-bold px-3 py-1 rounded-full uppercase self-center md:self-auto">
              Pro Member
            </span>
          </div>
          <p class="text-gray-500 font-medium mb-4">Senior Project Manager at People Solution</p>
          
          <div class="flex flex-wrap justify-center md:justify-start gap-4">
            <button class="bg-[#4a7c3f] text-white px-6 py-2.5 rounded-xl font-bold shadow-lg shadow-[#4a7c3f]/20 hover:-translate-y-0.5 transition-all">
              Edit Profile
            </button>
            <button class="bg-white border-2 border-gray-100 text-gray-600 px-6 py-2.5 rounded-xl font-bold hover:bg-gray-50 transition-all">
              Settings
            </button>
          </div>
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-10">
        <div class="bg-white p-6 rounded-[24px] border border-gray-100 shadow-sm flex items-center gap-5">
          <div class="w-14 h-14 bg-[#4a7c3f]/10 rounded-2xl flex items-center justify-center text-[#4a7c3f]">
            <i class="fa-solid fa-briefcase text-xl"></i>
          </div>
          <div>
            <p class="text-gray-400 text-sm font-bold uppercase tracking-wider">Projects</p>
            <p class="text-2xl font-black text-gray-900">12</p>
          </div>
        </div>

        <div class="bg-white p-6 rounded-[24px] border border-gray-100 shadow-sm flex items-center gap-5">
          <div class="w-14 h-14 bg-[#4a90a4]/10 rounded-2xl flex items-center justify-center text-[#4a90a4]">
            <i class="fa-solid fa-check-double text-xl"></i>
          </div>
          <div>
            <p class="text-gray-400 text-sm font-bold uppercase tracking-wider">Completed</p>
            <p class="text-2xl font-black text-gray-900">84</p>
          </div>
        </div>

        <div class="bg-white p-6 rounded-[24px] border border-gray-100 shadow-sm flex items-center gap-5">
          <div class="w-14 h-14 bg-yellow-100 rounded-2xl flex items-center justify-center text-yellow-600">
            <i class="fa-solid fa-star text-xl"></i>
          </div>
          <div>
            <p class="text-gray-400 text-sm font-bold uppercase tracking-wider">Reviews</p>
            <p class="text-2xl font-black text-gray-900">4.9</p>
          </div>
        </div>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-3 gap-10">
        <div class="lg:col-span-2 bg-white rounded-[32px] p-8 border border-gray-100 shadow-sm">
          <h3 class="text-xl font-black text-gray-900 mb-6 flex items-center gap-2">
            <span class="w-2 h-6 bg-[#4a7c3f] rounded-full"></span>
            Recent Activities
          </h3>
          
          <div class="space-y-6">
            <div v-for="i in 3" :key="i" class="flex items-start gap-4 pb-6 border-b border-gray-50 last:border-0">
              <div class="w-10 h-10 rounded-full bg-gray-100 flex items-center justify-center shrink-0">
                <i class="fa-solid fa-file-lines text-gray-400"></i>
              </div>
              <div>
                <p class="text-gray-900 font-bold">Updated "Q1 Financial Report"</p>
                <p class="text-gray-400 text-sm">Yesterday at 4:30 PM • Finance Department</p>
              </div>
            </div>
          </div>
        </div>

        <div class="bg-gradient-to-br from-[#4a7c3f] to-[#4a90a4] rounded-[32px] p-8 text-white relative overflow-hidden">
          <div class="absolute -top-10 -right-10 w-32 h-32 bg-white/10 rounded-full blur-2xl"></div>
          
          <h3 class="text-2xl font-black mb-4 relative z-10">Pro Tips</h3>
          <p class="text-white/80 font-medium mb-6 relative z-10 leading-relaxed">
            Completing your profile details increases your visibility to the People Solutions team by 40%.
          </p>
          
          <div class="bg-white/20 backdrop-blur-md rounded-2xl p-4 border border-white/30 relative z-10">
            <p class="text-xs font-bold uppercase mb-2">Profile Strength</p>
            <div class="w-full h-2 bg-white/20 rounded-full">
              <div class="h-full bg-white rounded-full w-[75%]"></div>
            </div>
            <p class="text-right text-xs mt-2 font-bold">75%</p>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
// Logic for fetching user data would go here
</script>

<style scoped>
h1, h3, p {
  font-family: Arial, sans-serif;
}
</style>