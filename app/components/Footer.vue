<template>
    <div class="bg-blue-400 block">
        <div class="flex justify-around">
            <!-- lefl footer -->
            <div class="block" >
                <!--logo-->

                <br>

                <div class="block ml-[60px]">
                    <p class="text-gray-50 text-[18px]">
                        Leading HR consulting firm in Cambodia providing comprehensive 
                        <br>human resource solutions and strategic workforce management 
                        <br>services.
                    </p>
                </div>

                <br>

                <div class="flex ml-[60px] text-[18px] gap-[10px]">
                    <span class="rounded-[360px] bg-yellow-500 w-[30px] h-[30px] justify-center flex">
                        <i class="fa-solid fa-location-dot mt-[5px] text-blue-400"></i>
                    </span>
                    <p class="text-gray-50 text-[18px]">
                        #306BCD, 3rd Floor, Monivong Boulevard, Phnom Penh, Cambodia
                    </p>
                </div>

                <br>

                <div class="flex ml-[60px] text-[18px] gap-[10px]">
                    <span class="rounded-[360px] bg-yellow-500 w-[30px] h-[30px] justify-center flex">
                        <i class="fa-regular fa-envelope mt-[5px] text-blue-400"></i>
                    </span>
                    <p class="text-gray-50 text-[18px]">
                        info@premiumhumanresources.com
                    </p>
                </div>

                <br>

                <div class="flex ml-[60px] text-[18px] gap-[10px]">
                    <span class="rounded-[360px] bg-yellow-500 w-[30px] h-[30px] justify-center flex">
                        <i class="fa-solid fa-phone mt-[5px] text-blue-400"></i>
                    </span>
                    <p class="text-gray-50 text-[18px]">
                        +855 012 902 527 
                    </p>
                </div>

                <br>

            </div>
            <!--end lefl footer-->
            <!--start right footer-->
            <div class="flex mt-[30px] text-gray-50 ">
                 <div class="flex flex-col gap-4">

        <!-- Heading -->
        <h4 class="text-white text-[18px] font-bold tracking-widest uppercase relative w-fit mr-[100px]
                after:absolute after:bottom-[-8px] after:left-0
                after:w-full after:h-[3px] after:bg-yellow-400 after:rounded-full">
        Quick Links
        </h4>

    <!-- Links -->
    <nav class="flex flex-col gap-2 mt-3">
      <NuxtLink
        v-for="link in quickLinks"
        :key="link.label"
        :to="link.to"
        class="flex items-center gap-2 text-blue-100 text-[15px] font-medium
               group w-fit transition-all duration-300
               hover:text-yellow-300 hover:translate-x-1"
      >
        <!-- Arrow icon -->
        <span class="text-yellow-400 text-[12px] transition-transform duration-300 group-hover:translate-x-1">
          &#9656;
        </span>
        {{ link.label }}
      </NuxtLink>
    </nav>

  </div>
                <div class="flex flex-col gap-4">
        <h4 class="text-white text-[17px] font-bold tracking-wider uppercase mr-[100px]
                   pb-2 border-b-2 border-yellow-400 w-fit">
          Follow Us
        </h4>
        <div class="flex flex-col gap-3">

          <!-- Telegram -->
          <a href="#"
             class="flex items-center gap-3 group w-fit">
            <span class="w-9 h-9 rounded-full bg-white/10 border border-white/20 flex items-center justify-center
                         group-hover:bg-[#2AABEE] group-hover:border-[#2AABEE] transition-all duration-300 shadow">
              <i class="fa-brands fa-telegram text-white text-[15px]"></i>
            </span>
            <span class="text-blue-100 text-[14px] group-hover:text-white transition-colors duration-200">Telegram</span>
          </a>

          <!-- TikTok -->
          <a href="#"
             class="flex items-center gap-3 group w-fit">
            <span class="w-9 h-9 rounded-full bg-white/10 border border-white/20 flex items-center justify-center
                         group-hover:bg-black group-hover:border-black transition-all duration-300 shadow">
              <i class="fa-brands fa-tiktok text-white text-[15px]"></i>
            </span>
            <span class="text-blue-100 text-[14px] group-hover:text-white transition-colors duration-200">TikTok</span>
          </a>

          <!-- Facebook -->
          <a href="#"
             class="flex items-center gap-3 group w-fit">
            <span class="w-9 h-9 rounded-full bg-white/10 border border-white/20 flex items-center justify-center
                         group-hover:bg-[#1877F2] group-hover:border-[#1877F2] transition-all duration-300 shadow">
              <i class="fa-brands fa-facebook-f text-white text-[15px]"></i>
            </span>
            <span class="text-blue-100 text-[14px] group-hover:text-white transition-colors duration-200">Facebook</span>
          </a>

        </div>
      </div>
            </div>
        </div>

        <!--last foot-->
        <hr>
        <div class="flex">
            <h3 class="m-auto text-[22px] p-[20px] text-gray-50">
                © 2023 Human Resource Service. All rights reserved.
            </h3>
        </div>
    </div>
</template>
<script setup>
const quickLinks = [
  { label: 'Home',            to: '/'         },
  { label: 'About Us',        to: '/about'    },
  { label: 'Services',        to: '/services' },
  { label: 'News & Insights', to: '/news'     },
  { label: 'Contact Us',      to: '/contact'  },
]
</script>