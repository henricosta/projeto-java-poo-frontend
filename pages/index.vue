<script setup lang="ts">
definePageMeta({
  layout: 'guest'
})
</script>

<template>
    <div>
        <div>
            <FormSearchVaga />
        </div>
        <div class="flex justify-center">
            <CardVaga class="w-1/3"/>
            <div class="w-1/2">
                <PageVaga />
            </div>
        </div>
    </div>
</template>
  