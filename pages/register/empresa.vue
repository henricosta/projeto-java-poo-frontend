<script setup lang="ts">
definePageMeta({
  layout: 'guest'
})
</script>

<template>
  <div class="flex justify-center">
    <Section class="w-2/6">
      <h1 class="text-3xl mb-6" id="titulo">Cadastre a sua empresa</h1>
      <form @submit.prevent>
        <div>
          <label for="nome_empresa">Nome da empresa</label>
          <input id="nome_empresa" type="text" class="mt-1 block w-full border">
        </div>
        <div class="flex justify-between mt-4">
          <div>
            <label for="cnpj">CNPJ</label>
            <input id="cnpj" type="text" class="mt-1 block w-full border">
          </div>
          <div>
            <label for="cep">CEP da Empresa</label>
            <input id="cep" type="text" class="mt-1 block w-full border">
          </div>
        </div>
        <div class="flex justify-between mt-4">
          <div>
            <label for="email">Email</label>
            <input id="email" type="text" class="mt-1 block w-full border">
          </div>
          <div>
            <label for="phone">Telefone</label>
            <input id="phone" type="text" class="mt-1 block w-full border">
          </div>
        </div>
        <div>
          <label for="password">Senha</label>
          <input id="password" type="text" class="mt-1 block w-full border">
        </div>
        <div class="flex items-center justify-end mt-4">
          <NuxtLink
            class="underline text-sm text-gray-600 hover:text-gray-900 rounded-md focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
            to="/login/empresa">Já possui registro?</NuxtLink>

          <button class="ml-4">
            Registrar empresa
          </button>
        </div>
      </form>
    </Section>
  </div>
</template>