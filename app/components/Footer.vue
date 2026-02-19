<template>
    <div class="bg-gray-600 block">
        <div class="flex justify-around">
            <!-- lefl footer -->
            <div class="block" >
                <!--logo-->
                <div>
                    <NuxtLink to="/" class="flex items-center gap-2 shrink-0 mt-12.5 ml-12.5">

                        <!-- PS Monogram -->
                        <div class="flex items-end">

                        <!-- P with person icon -->
                        <div class="flex flexafter:bottom-[-8px] after:left-0-col items-center">
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
                </div>

                <br>

                <div class="block ml-15">
                    <p class="text-gray-50 text-[18px]">
                        Leading HR consulting firm in Cambodia providing comprehensive 
                        <br>human resource solutions and strategic workforce management 
                        <br>services.
                    </p>
                </div>

                <br>

                <div class="flex ml-15 text-[18px] gap-2.5">
                    <span class="rounded-[360px] bg-yellow-500 w-7.5 h-7.5 justify-center flex">
                        <i class="fa-solid fa-location-dot mt-1.75"></i>
                    </span>
                    <p class="text-gray-50 text-[18px]">
                        #306BCD, 3rd Floor, Monivong Boulevard, Phnom Penh, Cambodia
                    </p>
                </div>

                <br>

                <div class="flex ml-15 text-[18px] gap-2.5">
                    <span class="rounded-[360px] bg-yellow-500 w-7.5 h-7.5 justify-center flex">
                        <i class="fa-regular fa-envelope mt-1.75 "></i>
                    </span>
                    <p class="text-gray-50 text-[18px]">
                        info@premiumhumanresources.com
                    </p>
                </div>

                <br>

                <div class="flex ml-15 text-[18px] gap-2.5">
                    <span class="rounded-[360px] bg-yellow-500 w-7.5 h-7.5 justify-center flex">
                        <i class="fa-solid fa-phone mt-1.75 "></i>
                    </span>
                    <p class="text-gray-50 text-[18px]">
                        +855 012 902 527 
                    </p>
                </div>

                <br>

            </div>
            <!--end lefl footer-->
            <!--start right footer-->
            <div class="flex mt-7.5 text-gray-50 ">
                 <div class="flex flex-col gap-4">

        <!-- Heading -->
        <h4 class="text-white text-[18px] font-bold tracking-widest uppercase relative w-fit mr-25
                after:absolute after:-bottom-2 after:left-0
                after:w-full after:h-0.75 after:bg-yellow-400 after:rounded-full mt-22.5">
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
       
        {{ link.label }}
      </NuxtLink>
    </nav>

  </div>
     <div class="flex flex-col gap-4">
        <h4 class="text-white text-[17px] font-bold tracking-wider uppercase mr-25
                   pb-2 border-b-2 border-yellow-400 w-fit mt-22.5">
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
            <h3 class="m-auto text-[15px] p-5 text-gray-50">
                Â© 2023 Human Resource Service. All rights reserved.
            </h3>
        </div>
    </div>
</template>
<script setup>
const quickLinks = [
  { label: 'Home',            to: '/'         },
  { label: 'About Us',       to: '/about'    },
  { label: 'Services',        to: '/services'  },
  { label: 'Blog',            to: '/blog'      },
  { label: 'Contact Us',      to: '/contact'   },
]
</script>