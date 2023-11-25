<script setup>
import axios from 'axios';
import { ref } from 'vue';

definePageMeta({
    layout: 'guest'
})

const { apiBase } = useRuntimeConfig().public;

const jobs = ref([])

const { data } = await axios.get(apiBase + '/jobs/list')

jobs.value = data.content

</script>

<template>
    <div>
        <div>
            <FormSearchVaga />
        </div>
        <div v-if="jobs" class="flex justify-center">
            <div class="w-1/3 max-h-screen overflow-auto">
                <CardVaga v-for="j in jobs" :key="j.id" :job="j" />
            </div>
            <div class="w-1/2">
                <PageVaga :job="jobs[0]" />
            </div>
        </div>
        <div v-else>
            <h1>nenhuma vaga encontrada</h1>
        </div>
    </div>
</template>
  