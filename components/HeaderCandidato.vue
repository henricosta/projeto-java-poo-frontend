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
                        <NuxtLink to="/">Buscar vagas</NuxtLink>
                        <NuxtLink to="/">Minhas vagas</NuxtLink>
                    </div>
                </div>
                <!-- Botões da direita -->
                <NuxtLink to="/perfil/candidato">

                    <div class="relative w-10 h-10 overflow-hidden bg-gray-100 rounded-full dark:bg-gray-600 mr-4 mt-3">
                        <svg class="absolute w-12 h-12 text-gray-400 -left-1" fill="currentColor" viewBox="0 0 20 20"
                            xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
                                clip-rule="evenodd"></path>
                        </svg>
                    </div>

                </NuxtLink>
            </div>
        </nav>
    </header>
</template>
