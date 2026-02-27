<script setup>

</script>
<template>
    <div class="w-[93%] bg-gray-50 max-w-(--ui-container) mx-auto px-4 sm:px-6 py-6">
        <div class="flex">
            <img src="../assets/images/Network-engineer.webp" alt="" class="w-250 h-75 m-auto rounded-lg ">
        </div>
        <div class="flex gap-4">
            <article class="flex-1 flex flex-col gap-y-3">
                <header class="bg-base-100 rounded-md ">
                    <div class="overflow-hidden relative">
                        <div class="flex p-4 gap-x-4 ">
                            <div class="block ">
                                <h1 class="font-bold text-3xl leading-11  pr-42 text-blue-500 mt-2.5">
                                    Networking Engineer
                                </h1>
                                <div class="flex gap-4 text-sm mt-2 text-gray-600 dark:text-gray-400 ">
                                    <p class="flex gap-x-1 items-center">
                                        <span> ID : 12345</span> /
                                    </p>
                                    <p class="flex gap-x-1 items-center">
                                        <span class="icontify ik-24:p-location-outline text-md">
                                            <img class="w-5 h-5" src="../assets/images/location.png" alt="location">
                                        </span>
                                        Chbar Ompov /
                                    </p>
                                    <time class="flex gap-x-1 items-center " datetime="2026:02:23 14:06">
                                        <span class="icintify i-k24:p-history text-md ">2026:02:23 14:06</span>
                                    </time>
                                </div>

                                <div class="flex gap-2 mt-2 items-center ">
                                    <p class="flex font-bold text-2xl text-error-300">
                                        <span>
                                            <i class="fa-solid fa-dollar-sign"></i>
                                            250 
                                            <i class="fa-solid fa-plus"></i>
                                        </span>
                                    </p>
                                </div>

                            </div>

                        </div>

                        <!-- button apply job -->
                        <div class="shadow-xl hover:shadow-yellow-500 bg-yellow-400 p-1.25 text-black-50 w-35">
                            <NuxtLink to="/#" class="" type="button">
                                Apply For this Job
                            </NuxtLink>
                        </div>

                    </div>
                </header>   

                <!-- description about this job -->
                <section class="p-4 bg-base-100 rounded-md flex flex-col gap-y-6">
                    <h2 class="font-bold text-3xl leading-11 text-blue-500">Description</h2>
                    <div class="grid grid-cols-5 gap-x-6 gap-y-4">
                        <dl class="">
                            <dt class="text-sm text-gray dark:text-gray-400">Main Categories</dt>
                            <dd class="text-primary-600 cursor-pointer hover:underline">Jobs</dd>
                        </dl>

                        <dl class="">
                            <dt class="text-sm text-gray dark:text-gray-400">Categories</dt>
                            <dd class="text-primary-600 cursor-pointer hover:underline">Information Technology</dd>
                        </dl>

                        <dl class="">
                            <dt class="text-sm text-gray dark:text-gray-400">Main Categories</dt>
                            <dd class="text-primary-600 cursor-pointer hover:underline">Jobs</dd>
                        </dl>

                        <dl class="">
                            <dt class="text-sm text-gray dark:text-gray-400">Jobs Type</dt>
                            <dd class="text-primary-600 cursor-pointer hover:underline">Full-time</dd>
                        </dl>

                        <dl class="">
                            <dt class="text-sm text-gray dark:text-gray-400">Experience</dt>
                            <dd class="text-primary-600 cursor-pointer hover:underline">1year+</dd>
                        </dl>

                    </div>

                    <!-- list_info -->
                    <p class="text-base/8 whitespace-break-spaces wrap-break-word break-all leading-8 max-w-3xl ">
                        Network-Engineer <br>   
                        Junior Level/Entry  <br><br><br>

                        Working Days: Monday ~ Friday <br>
                        Working Hours: 8:00 AM ~ 5:00 PM <br><br><br>

                        Salary: Negotiate based on experience <br><br>

                        Technical Skills: <br>
                        • End-user devices (laptops, desktops, peripherals) <br>
                        • Networking (LAN, internet, connectivity) <br>
                        • Linux servers (basic hosting & dev support) <br>
                        • Virtual machines <br>
                        • Daily operations & troubleshooting <br>
                        • Set up and manage virtual machines using VirtualBox, VMware, or Hyper-V <br>
                        • Configure virtual environments for development and testing <br><br>

                        Key Responsibilities <br>
                        • Support and maintain office IT infrastructure, including laptops, desktops, and peripheral<br>
                        devices
                        • Set up, configure, and troubleshoot network connectivity between users and systems <br>
                        • Assist users with daily technical issues related to hardware, software, and network access <br>
                        • Help manage and monitor basic network equipment (routers, switches, access points) <br>
                        • Support Linux servers used for development and hosting purposes <br>
                        • Assist with virtual machine setup and basic management <br>
                        • Document issues, solutions, and configurations as needed <br><br>

                        Skills & Qualifications <br>
                        • Able to work under pressure and handle multiple tasks at the same time <br>
                        • Strong willingness to learn and improve technical skills <br>
                        • Good problem-solving and troubleshooting mindset <br>
                        • Able to communicate clearly in English (spoken and written) <br>
                        • Team-oriented with a positive and responsible attitude <br><br><br>

                        --->Apply to: <br>
                        Email:info@premiumhumanresources.com <br>
                        <p class="flex gap-2">Telegram: 
                            <span class="flex gap-2"> 
                            <img class="flex rounded-sm w-5 h-5" src="../assets/images/sim-smart.jpeg" alt="sim-smart">
                                +855 92 95 04 77</span>
                        </p>
                    </p>

                    <!-- location for find company -->
                    <div class="flrx gap-x-3">
                        <div class="flex">
                            <span class="flex gap-5"><img class="w-5 h-5" src="../assets/images/location.png" alt=""></span>
                        </div>

                        <div class="flex-1 ">
                            <p class="font-semibold">Tonle Basak, Chamkar Mon, Phnom Penh</p>

                        </div>

                    </div>

                </section>

            </article>

            <!-- left-side -->
            

        </div>
    </div>

</template>
