<script setup lang="ts">
import axios from 'axios';

definePageMeta({
  layout: 'guest'
})


const { apiBase } = useRuntimeConfig().public;

const email = ref('')
const password = ref('')

async function sendLoginRequest() {
  const request = await axios.post(apiBase + '/auth/login/company', {
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
  <div class="flex justify-center items-center mt-14">
    <Section>
      <div>
        <h1 class="text-2xl mb-3"><strong>Entrar como empresa</strong></h1>
        <form @submit.prevent>
          <div>
            <label for="email">Email</label>
            <input v-model="email" id="email" type="text" class="mt-1 block w-full border">
          </div>

          <div class="mt-4">
            <label for="password">Senha</label>
            <input v-model="password" id="password" type="password" class="mt-1 block w-full border">
          </div>

          <div class="flex items-center justify-end mt-4">
            <button class="ml-4 bg-amber-50 border-2 border-black text-black">
              <NuxtLink to="/register/empresa">Cadastrar-se</NuxtLink>
            </button>
            <button @click="sendLoginRequest" class="ml-4">
              Login
            </button>
          </div>
        </form>
      </div>
    </Section>
  </div>
</template>