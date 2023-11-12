<script setup lang="ts">
definePageMeta({
  layout: 'guest'
})
</script>

<template>
  <div class="flex justify-center items-center mt-14">
    <Section class="w-96">
      <h1 class="text-2xl mb-3"><strong>Criar conta</strong></h1>
      <form @submit.prevent>
        <div>
          <label for="name">Nome</label>
          <input id="name" type="text" class="mt-1 block w-full border">
        </div>

        <div>
          <label for="email">Email</label>
          <input id="email" type="text" class="mt-1 block w-full border">
        </div>

        <div>
          <label for="password">Senha</label>
          <input id="password" type="text" class="mt-1 block w-full border">
        </div>

        <div class="flex items-center justify-end mt-4">
          <NuxtLink to="/login/candidato"
            class="ml-4 bg-gray-100 px-2 py-1 rounded-md border text-black hover:bg-gray-200 ">Já tem conta?</NuxtLink>
          <button class="ml-4">
            Criar conta
          </button>
        </div>
      </form>
    </Section>
  </div>
</template>