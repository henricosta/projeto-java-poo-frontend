<template>
    <form @submit.prevent id="form-busca-vaga">
        <div class="bg-gray-50 flex justify-center">
            <div class="py-8 flex">
                <input type="text" placeholder="Ex: Desenvolvedor web" class="border w-96 rounded-r-none px-4"/>
                <button type="submit" class="px-4 py-4 rounded-l-none border bg-black text-white">Buscar vaga</button>
            </div>
        </div>
    </form>
</template>