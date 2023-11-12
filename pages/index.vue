<script setup>
definePageMeta({
  layout: 'guest'
})

const { data: vagas } = await useFetch('http://localhost:8080/vagas/list')

</script>

<template>
    <div>
        <div>
            <FormSearchVaga />
        </div>
        <div class="flex justify-center">
            <div class="w-1/3 max-h-screen overflow-auto">
                {{ console.log(vagas.content) }}
                <CardVaga v-for="v in vagas.content" :key="v.id" :title="v.title" :description="v.description" :modalidade="v.modalidade" :cidade="v.cidade" :nome-empresa="v.empresa.name" />
            </div>
            <div class="w-1/2">
                <PageVaga v-if="vagas.content[0]" :title="vagas.content[0].title" :description="vagas.content[0].description" :modalidade="vagas.content[0].modalidade" :cidade="vagas.content[0].cidade" :nome-empresa="vagas.content[0].empresa.name"/>
            </div>
        </div>
    </div>
</template>
  