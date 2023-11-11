<template>
    <form @submit.prevent id="form-busca-vaga">
        <div class="bg-gray-50 flex justify-center">
            <div class="py-8 flex">
                <input type="text" placeholder="Ex: Desenvolvedor web" class="border w-96 rounded-r-none px-4"/>
                <button type="submit" class="px-4 py-4 rounded-l-none border bg-black text-white">Buscar vaga</button>
            </div>
        </div>
        <div class="border-t shadow-sm bg-gray-50 py-4 flex justify-center">
            <button class="rounded-full border border-gray-800 hover:bg-gray-700 text-white bg-gray-800 px-5 mr-5">Redefinir filtros</button>
            <select class="py-2 mx-2 border">
                <option value="0" disabled selected>Cidade</option>
            </select>
            <select class="py-2 mx-2 border">
                <option value="0" disabled selected>Modalidade</option>
            </select>
        </div>
    </form>
</template>