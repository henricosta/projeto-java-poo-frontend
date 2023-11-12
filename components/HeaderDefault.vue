<template>
    <header>
        <nav class="bg-white border-b border-gray-100">
            <div class="flex flex-wrap justify-between text-gray-800 h-16">
                <div class="flex">
                    <!-- Logo -->
                    <div class="flex shrink-0 items-center mx-10">
                        <a href="/" class="text-gray-900">
                        VAGAS
                        </a>
                    </div>
                    <!-- Navigation Links -->
                    <div class="flex items-center">
                        <NuxtLink to="/" class="mr-3">Buscar vagas</NuxtLink>
                        <NuxtLink to="/register/empresa">Para empresas</NuxtLink>
                    </div>
                </div>
                <!-- Botões da direita -->
                <div class="flex items-center mr-8">
                    <div>
                        <NuxtLink to="/login/candidato">Entrar</NuxtLink>
                        <NuxtLink to="/register/candidato" class="ml-3 border bg-gray-900 text-white rounded-md px-3 py-2">Cadastre-se</NuxtLink>
                    </div>
                </div>
            </div>
        </nav>
    </header>
</template>
