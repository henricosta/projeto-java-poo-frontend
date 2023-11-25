<script setup>
defineProps({
    job: Object
})

</script>

<template>
    <div class=" bg-white shadow-sm mx-6 border rounded-lg mt-3">
        <div class="m-14">
            <h2 class="text-3xl mb-2">{{ job.title }}</h2>
            <p class="text-gray-800">{{ job.type }}</p>
            <button class="px-2 py-3 mt-4">Candidatar-se</button>
            <hr class="my-1">
            <p id="descricao-vaga" class="descricao">{{ job.description }}</p>
        </div>
    </div>
</template>
