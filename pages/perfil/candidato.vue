<script setup lang="ts">
definePageMeta({
    layout: 'candidato'
})
</script>

<template>
    <div>
        <Section>
            <div
                class="mb-8 relative inline-flex items-center justify-center w-60 h-60 overflow-hidden bg-gray-100 rounded-full dark:bg-gray-600">
                <span class="font-medium text-gray-600 dark:text-gray-300">JL</span>
            </div>
            <div>
                <div class="mb-3 text-4xl font-extrabold dark:text-white">Nome Completo</div>
                <ul class="max-w-md space-y-1 text-gray-500 list-none list-inside dark:text-gray-400">
                    <li>email@email.com</li>
                    <li>9999999999</li>
                </ul>
            </div>
        </Section>
        <Section>
            <div>
                <h4 class="inline-block mb-2 text-lg font-semibold text-gray-900 dark:text-white">Competências</h4>
                <button type="button"
                    class="ml-3 text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-full text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700">Adicionar
                    competência</button>
            </div>
            <div>
                <ul class="space-y-1 text-gray-500 list-disc list-inside dark:text-gray-400">
                    <li class="hover:bg-gray-100 flex items-center justify-between py-1 px-3 rounded-lg w-full"
                        style="text-transform: capitalize">
                        <p>nome da competencia</p>
                        <button class="border py-1 px-3 rounded-lg hover:bg-red-600 hover:text-white">Deletar</button>
                    </li>
                </ul>
            </div>
        </Section>
        <Section>
            <div>
                <h4 class="inline-block mb-2 text-lg font-semibold text-gray-900 dark:text-white">Formações</h4>
                <button type="button"
                    class="ml-3 text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-full text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700">Adicionar
                    formação</button>
            </div>
            <div>
                <div>
                    <hr>
                    <div class="flex items-center justify-between mt-2">
                        <h1 class="text-xl">Instituicao</h1>
                        <button class="px-3 py-1 text-sm bg-gray-300 rounded-md hover:bg-gray-400">Editar</button>
                    </div>
                    <div class="mb-2 mt-2 text-gray-700">descricao da formacao</div>
                </div>
            </div>
        </Section>
        <Section>
            <button class="bg-gray-800 rounded-md text-white px-3 py-2">Logout</button>
        </Section>
    </div>
</template>