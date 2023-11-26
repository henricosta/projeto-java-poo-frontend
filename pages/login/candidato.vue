<script setup lang="ts">
import axios from 'axios';

definePageMeta({
  layout: 'guest'
})

const { apiBase } = useRuntimeConfig().public;

const email = ref('')
const password = ref('')

async function sendLoginRequest() {
  const request = await axios.post(apiBase + '/auth/login/candidate', {
    email: email.value,
    password: password.value
  })

  if (request.status == 200) {
    const { token } = request.data
    // TODO: Set to local storage
    console.log(token)
    // localStorage.setItem('token', token)
  }

  // console.log(localStorage.getItem('token'))
}


</script>

<template>
  <div class="flex justify-center">
    <Section class="w-3/12 mt-16 rounded-md p-8">
      <h1 class="text-2xl mb-3"><strong>Login</strong></h1>
      <form @submit.prevent>
        <div>
          <label for="email">Email</label>
          <input v-model="email" id="email" type="text" class="mt-1 block w-full border">
        </div>

        <div>
          <label for="password">Senha</label>
          <input v-model="password" id="password" type="password" class="mt-1 block w-full border">
        </div>

        <div class="flex items-center justify-end mt-4">
          <NuxtLink to="/register/candidato" class="ml-4 px-2 py-1  text-blue-500 underline ">Cadastrar-se</NuxtLink>
          <button class="ml-4 border rounded-md px-3 py-2 hover:bg-gray-800 hover:text-white"
            @click="sendLoginRequest">
            Entrar
          </button>
        </div>
      </form>
    </Section>
  </div>
</template>