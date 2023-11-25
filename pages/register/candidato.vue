<script setup lang="ts">
import axios from 'axios';

definePageMeta({
  layout: 'guest'
})

const { apiBase } = useRuntimeConfig().public;

const name = ref('')
const email = ref('')
const password = ref('')

async function postCandidateRegister() {
  console.log(name, email, password)
  const response = await axios.post(apiBase + '/auth/register/candidate', {
    name: name.value,
    email: email.value,
    password: password.value
  })

  console.log(response)
}
</script>

<template>
  <div class="flex justify-center items-center mt-14">
    <Section class="w-96">
      <h1 class="text-2xl mb-3"><strong>Criar conta</strong></h1>
      <form @submit.prevent>
        <div>
          <label for="name">Nome</label>
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
          <NuxtLink to="/login/candidato"
            class="ml-4 bg-gray-100 px-2 py-1 rounded-md border text-black hover:bg-gray-200 ">Já tem conta?</NuxtLink>
          <button class="ml-4" @click="postCandidateRegister">
            Criar conta
          </button>
        </div>
      </form>
    </Section>
  </div>
</template>