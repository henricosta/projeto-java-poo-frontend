<script setup>
defineProps({
  job: Object
})
</script>

<template>
    <div class="bg-white block p-8 border shadow-sm h-48 rounded-lg my-3 mx-5">
        <h5 class="mb-1 text-xl text-gray-900"><strong>{{ job.title }}</strong></h5>
        <p class="mb-1 text-gray-600 text-sm">{{ job.type }}</p>
        <p class="text-sm" id="card-text">{{ job.description }}</p>
    </div>
</template>
