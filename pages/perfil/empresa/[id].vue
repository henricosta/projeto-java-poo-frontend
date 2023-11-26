<script setup>
import axios from 'axios';

// TODO: Mudar layout
definePageMeta({
  layout: 'guest'
})

const { apiBase } = useRuntimeConfig().public
const route = useRoute()


const company = ref({})
const { data } = await axios.get(apiBase + '/companies/details', {
  params: {
    company_id: route.params.id
  }
})
company.value = data
// const { data: empresa } = await useFetch("http://localhost:8080/empresas/" + route.params.id + "/profile")
</script>

<template>
  <div>
    <Section>
      {{ console.log(company) }}
      <div
        class="mb-8 relative inline-flex items-center justify-center w-60 h-60 overflow-hidden bg-gray-100 rounded-full dark:bg-gray-600">
        <svg class="absolute w-full h-full text-gray-400 mt-12" fill="currentColor" viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd"></path>
        </svg>
      </div>
      <div class="flex items-center">
        <div class="mb-3 text-4xl font-extrabold dark:text-white">{{ company.name }}</div>
        <button class="ml-4 mb-2 py-2 px-3 rounded-md border bg-gray-200 shadow-sm text-sm hover:bg-gray-400">Editar
          informações</button>
      </div>
      <ul class="max-w-md space-y-1 text-gray-500 list-none list-inside dark:text-gray-400">
        <li>{{ company.email }}</li>
      </ul>
    </Section>
    <Section class="mr-8">
      <div class="flex items-center">
        <h1 class="text-2xl">Vagas publicadas</h1>
        <button class="shadow-sm rounded-lg border px-3 py-2 bg-gray-800 text-white hover:bg-gray-700">Adicionar
          vaga</button>
      </div>
      <hr class="mt-2 mb-3">
      <!-- <CardVagaSmall /> -->
    </Section>
  </div>
</template>