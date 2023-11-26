<script setup lang="ts">
import axios from 'axios';
// TODO: Change layout based on authentication
definePageMeta({
  layout: 'guest'
})

const { apiBase } = useRuntimeConfig().public

const name = ref('')
const email = ref('')
const password = ref('')

async function postCompanyRegister() {
  console.log(name, email, password)
  const response = await axios.post(apiBase + '/auth/register/company', {
    name: name.value,
    email: email.value,
    password: password.value
  })

  console.log(response)
}
</script>

<template>
  <div class="flex justify-center">
    <Section class="w-2/6 mt-16 p-8">
      <h1 class="text-2xl mb-6" id="titulo">Cadastre a sua empresa</h1>
      <form @submit.prevent>
        <div>
          <label for="name">Nome da empresa</label>
          <input v-model="name" id="name" type="text" class="mt-1 block w-full border">
        </div>

        <div>
          <label for="email">Email</label>
          <input v-model="email" id="email" type="text" class="mt-1 block w-full border">
        </div>

        <div>
          <label for="password">Senha</label>
          <input v-model="password" id="password" type="password" class="mt-1 block w-full border">
        </div>
        <div class="flex items-center justify-end mt-4">
          <NuxtLink to="/login/empresa"
            class="ml-4 px-2 py-1  text-blue-500 underline ">Entrar</NuxtLink>
          <button class="ml-4 border rounded-md px-3 py-2 hover:bg-gray-800 hover:text-white" @click="postCompanyRegister">
            Cadastrar empresa
          </button>
        </div>
      </form>
    </Section>
  </div>
</template>