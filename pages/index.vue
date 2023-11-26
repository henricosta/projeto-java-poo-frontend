<script setup>
import axios from 'axios';
import { ref } from 'vue';

definePageMeta({
    layout: 'guest'
})

const { apiBase } = useRuntimeConfig().public;

const jobs = ref([])

// Primeiro carregamento da página
const { data } = await axios.get(apiBase + '/jobs/list')
jobs.value = data.content

// Funcão feita para ser passada como props para outros componentes
// Atualiza a lista usando o ref jobs
async function searchJobs(title, type) {
    
    const { data } = await axios.get(apiBase + '/jobs/list', {
        params: {
            title: title || null,
            type: type === '0' ? null : type 
        }
    })

    jobs.value = data.content
}

const currentJob = ref(jobs.value[0])

function updateCurrentPageJob(job) {
    currentJob.value = job
}

</script>

<template>
    <div>
        <div>
            <FormSearchVaga :searchJobsFunction="searchJobs"/>
        </div>
        <div v-if="jobs.length > 0" class="flex justify-center">
            <div class="w-1/3 max-h-screen overflow-auto">
                <CardVaga v-for="j in jobs" :key="j.id" :job="j" @click="() => updateCurrentPageJob(j)" />
            </div>
            <div class="w-1/2">
                <PageVaga :job="currentJob"/>
            </div>
        </div>
        <div v-else class="flex justify-center">
            <h1 class="text-2xl mt-5">Nenhuma vaga encontrada</h1>
        </div>
    </div>
</template>
  