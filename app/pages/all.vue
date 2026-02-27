<template>
    <div v-for="text in prop.slice(1, 5)" :key="text.id"  class="">
            {{ text.skill_name }}
            
    </div>
</template>


<script setup>
import axios from 'axios';


const key = "5cfebb07d4c1eea7806b3407c1e8de1b0b7fd46fccd8c4c582cf7edb4968beee98f9112e8a022f0d657138f6701dfeb78b78303c70378f8948d7f151a17564894c647bd9314b857aa906a7b6297d08fa6fa73e52cd52d1abe282c42626555b2ade9be92a425fb93bfc98c2d14a37928deee3bbf98a512b231ec6c99800bc0748";
const api = await axios.get('http://localhost:1337/api/skills',
    {
        headers: {
            Authorization : `Bearer ${key}`
        }
    }
);
const prop = api.data.data
console.log(prop)

</script>