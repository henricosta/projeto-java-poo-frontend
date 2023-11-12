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
    <div class=" bg-white shadow-sm mx-6 border rounded-lg mt-3">
        <div class="m-14">
            <h2 class="text-3xl mb-2">{{ title }}</h2>
            <p class="text-gray-800">{{ cidade }} - ({{modalidade}})</p>
            <p class="text-gray-800">{{ nomeEmpresa }}</p>
            <button class="px-2 py-3 mt-4">Candidatar-se</button>
            <hr class="my-1">
            <p id="descricao-vaga" class="descricao">{{ description }}</p>
        </div>
    </div>
</template>
