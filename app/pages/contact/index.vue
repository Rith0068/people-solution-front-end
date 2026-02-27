<template>
  <div class="bg-gray-100 min-h-screen font-sans">
    <section class="relative h-80 flex items-center justify-center bg-slate-900 overflow-hidden">
      <div 
        class="absolute inset-0 opacity-30 bg-cover bg-center"
        style="background-image: url('https://images.unsplash.com/photo-1534536281715-e28d76689b4d?auto=format&fit=crop&q=80&w=2070');"
      ></div>
      
      <div class="absolute inset-0 opacity-10 bg-[radial-gradient(#fff_1px,transparent_1px)] [background-size:20px_20px]"></div>
      
      <h1 class="relative z-10 text-white text-5xl font-bold tracking-tight">Contact Us</h1>
    </section>

    <section class="max-w-6xl mx-auto px-6 -mt-20 relative z-20 pb-20">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        
        <div 
          v-for="(item, index) in contactDetails" 
          :key="index"
          class="bg-white p-10 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-300 flex flex-col justify-between min-h-[220px]"
        >
          <div>
            <h3 class="text-slate-800 font-bold text-xl mb-3">{{ item.title }}</h3>
            <p class="text-gray-500 font-medium leading-relaxed whitespace-pre-line">
              {{ item.content }}
            </p>
          </div>
          
          <div class="flex justify-end">
            <div class="w-14 h-14 bg-[#E9C46A] rounded-full flex items-center justify-center text-slate-800 shadow-sm">
              <i :class="['fa-solid', item.icon, 'text-xl']"></i>
            </div>
          </div>
        </div>

      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const contactDetails = ref([
  {
    title: 'Phone Number',
    content: '+855 012 902 527',
    icon: 'fa-phone'
  },
  {
    title: 'Email Address',
    content: 'seyharaksa@people-solution.com',
    icon: 'fa-envelope'
  },
  {
    title: 'Our Location',
    content: '#306BCD, 3rd Floor, Monivong Boulevard, Phnom Penh, Cambodia',
    icon: 'fa-location-dot'
  }
]);
</script>

<style scoped>

.shadow-xl {
  transform: translateY(0);
}
.shadow-xl:hover {
  transform: translateY(-5px);
}
</style>