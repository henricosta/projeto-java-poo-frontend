<script setup>
defineProps({
  title: String,
  description: String,
  modalidade: String,
  cidade: String,
  nomeEmpresa: String
})
</script>

<template>
    <div class="bg-white block p-8 border shadow-sm h-48 rounded-lg my-3 mx-5">
        <h5 class="mb-1 text-xl text-gray-900"><strong>{{ title }}</strong></h5>
        <p class="text-gray-800">{{ nomeEmpresa }}</p>
        <p class="mb-1 text-gray-600 text-sm">{{ cidade }} - ({{ modalidade }})</p>
        <p class="text-sm" id="card-text">{{ description }}</p>
    </div>
</template>
