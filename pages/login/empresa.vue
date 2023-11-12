<script setup lang="ts">
definePageMeta({
  layout: 'guest'
})
</script>

<template>
  <div class="flex justify-center items-center mt-14">
    <Section>
      <div>
        <h1 class="text-2xl mb-3"><strong>Entrar como empresa</strong></h1>
        <form @submit.prevent>
          <div>
            <label for="email">Email</label>
            <input id="email" type="text" class="mt-1 block w-full border">
          </div>

          <div class="mt-4">
            <label for="password">Senha</label>
            <input id="password" type="text" class="mt-1 block w-full border">
          </div>

          <div class="flex items-center justify-end mt-4">
            <button class="ml-4 bg-amber-50 border-2 border-black text-black">
              <NuxtLink to="/register/empresa">Cadastrar-se</NuxtLink>
            </button>
            <button class="ml-4">
              Login
            </button>
          </div>
        </form>
      </div>
    </Section>
  </div>
</template>