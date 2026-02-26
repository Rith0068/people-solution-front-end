<script setup>
import Btjob from '~/components/Btjob.vue';
import CartJobsale from '~/components/CartJobsale.vue';
import { ref } from 'vue';

const showMore = ref(false)
</script>
<template>
    <Btjob />
    <CartJobsale class="xl:pl-[40px]"/>
    <div v-if="showMore" class="xl:pl-[40px]">
        <br>
        <CartJobsale />
        <br>
        <CartJobsale />
    </div>
    <div class="flex">
        
        <button @click="showMore = ! showMore" class="group relative flex items-center gap-3 px-6 py-2.5 overflow-hidden
             border shadow-xl rounded-sm bg-white/5 m-auto mt-[10px] mb-[10px]
             font-mono text-[0.65rem] tracking-widest uppercase text-slate-400
             transition-all duration-300 ease-out
             hover:border-lime-400 hover:text-lime-400
             hover:shadow-[0_0_20px_rgba(163,230,53,0.2),0_0_0_1px_rgba(163,230,53,1)]
             active:scale-95">
            <p>
                {{ showMore ? "Close" : "Show More..."}}
            </p>
        </button>
        
    </div>
    

</template>
