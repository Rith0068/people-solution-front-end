<script setup>
import axios from 'axios';
import { ref } from 'vue';

// 1. Correct typo: "Authrization" -> "Authorization" [1]
const config = {
    headers: {
        Authorization: 'Bearer 5cfebb07...[token]...2ade9be92a425fb93bfc98c2d14a37928deee3bbf98a512b231ec6c99800bc0748'
    }
}

// Ensure jobData is reactive
const jobData = ref([]);

try {
    // 2. Fixed variable name typo: dateFetch -> dataFetch
    const dataFetch = await axios.get('http://localhost:1337/api/job-postings', config);
    jobData.value = dataFetch.data.data;
    console.log(jobData.value);
} catch (error) {
    console.error('Error fetching data:', error);
}
</script>

<template>
    <h1>Job Postings</h1>
    <!-- 3. Added :key to v-for for better performance/behavior -->
    <div v-for="job in jobData" :key="job.id" class="job-item">
        {{ job.attributes?.salary_range || 'No salary listed' }}
    </div>
</template>
