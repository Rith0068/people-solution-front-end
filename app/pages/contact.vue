<template>
  <div class="bg-gray-100 min-h-screen font-sans antialiased">
    <section class="relative h-80 flex items-center justify-center bg-slate-900 overflow-hidden">
      <div class="absolute inset-0 opacity-30 bg-cover bg-center"
        style="background-image: url('https://images.unsplash.com/photo-1534536281715-e28d76689b4d?auto=format&fit=crop&q=80&w=2070');">
      </div>
      <div
        class="absolute inset-0 opacity-10 bg-[radial-gradient(#fff_1px,transparent_1px)] bg-size-20px-20px">
      </div>
      <h1 class="relative z-10 text-white text-5xl font-bold tracking-tight">Contact Us</h1>
    </section>

    <section class="max-w-7xl mx-auto px-6 -mt-20 relative z-20 pb-12">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div v-for="(item, index) in contactDetails" :key="index"
          class="bg-white p-10 rounded-2xl shadow-xl hover:shadow-2xl transition-all duration-300 flex flex-col justify-between min-h-55">
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

    <section class="bg-gray-50 py-16 px-4">
      <div class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-12 items-start">

        <div class="w-full h-125 rounded-2xl overflow-hidden shadow-sm border border-gray-200">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3618.9726075789513!2d104.88399937464044!3d11.544596844556093!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x310950549f27fc1b%3A0x65c2d5b055de0d9d!2sPSE%20-%20Pour%20un%20Sourire%20d&#39;Enfant!5e1!3m2!1sen!2skh!4v1771231986876!5m2!1sen!2skh"
            width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"></iframe>

        </div>
        <div class="flex flex-col">
          <div class="mb-4">
            <span
              class="bg-[#E9C46A] text-[#2D3E50] text-[10px] font-bold uppercase tracking-widest px-3 py-1 rounded-full">
              Make Custom Request
            </span>
          </div>
          <h2 class="text-[#2D3E50] text-4xl md:text-5xl font-bold mb-8 leading-tight">
            Let's Discuss Your HR Needs
          </h2>
          <form @submit.prevent="handleSubmit" class="space-y-4">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
              <input v-model="form.firstName" type="text" placeholder="First Name"
                class="border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-[#E9C46A]">
              <input v-model="form.lastName" type="text" placeholder="Last Name"
                class="border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-[#E9C46A]">
            </div>
            <input v-model="form.email" type="email" placeholder="Email Address"
              class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-[#E9C46A]">
            <input v-model="form.subject" type="text" placeholder="Subject"
              class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-[#E9C46A]">
            <textarea v-model="form.message" placeholder="Your Message" rows="5"
              class="w-full border border-gray-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-[#E9C46A]"></textarea>
            <button type="submit"
              class="bg-[#E9C46A] text-[#2D3E50] font-bold py-3 px-6 rounded-lg hover:bg-[#d8b45c] transition-colors">Send
              Message</button>
          </form>

        </div>


      </div>
    </section>

    <div class="fixed bottom-8 right-8">
      <button @click="scrollToTop"
        class="bg-[#E9C46A] w-12 h-12 rounded-lg flex items-center justify-center shadow-lg hover:-translate-y-1 transition-transform">
        <i class="fa-solid fa-arrow-up text-[#2D3E50]"></i>
      </button>
    </div>

    <div></div>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue';

// Contact Card Data
const contactDetails = ref([
  {
    title: 'Phone Number',
    content: '+855 096 222 1351',
    icon: 'fa-phone'
  },
  {
    title: 'Email Address',
    content: 'seyha@premiumhumanresources.com',
    icon: 'fa-envelope'
  },
  {
    title: 'Our Location',
    content: '#306BCD, 3rd Floor, Monivong Boulevard, Phnom Penh, Cambodia',
    icon: 'fa-location-dot'
  }
]);


const form = reactive({
  firstName: '',
  lastName: '',
  email: '',
  subject: '',
  message: ''
});

const handleSubmit = () => {
  console.log('Form Submitted:', form);
  alert('Thank you! Your inquiry has been sent.');
};

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};
</script>

<style scoped>
.shadow-xl {
  transform: translateY(0);
}

.shadow-xl:hover {
  transform: translateY(-5px);
}
</style>