<script setup>
    import { RouterLink } from 'vue-router';

</script>

<template>
    <header class="bg-slate-800">
        <div class="mx-auto container px-5 py-16">
            <div class="flex justify-between items-center">
                <div >
                    <RouterLink :to="{name: 'inicio'}">
                        <img class="w-32" src="/img/logo.svg" alt="logotipo">
                    </RouterLink>
                </div>
                <nav class="flex gap-4 ">
                    <RouterLink 
                        :to="{name: 'inicio'}" 
                        class="text-white uppercase font-bold"
                        active-class="text-orange-500"
                        >
                        Inicio
                    </RouterLink>
                    <RouterLink 
                        :to="{name: 'favoritos'}" 
                        class="text-white uppercase font-bold"
                        active-class="text-orange-500"
                        >
                        Favoritos
                    </RouterLink>
                </nav>
            </div>
            <form class="md:w-1/2 2xl:w-1/3 bg-orange-400 my-32 p-10 rounded-lg shadow space-y-6" action="">

                <div class="space-y-4 ">
                    <label  
                        class="block text-white uppercase font-extrabold text-lg" 
                        for="ingrediente">Nombre o ingredientes</label>
                    <input 
                        class="p-3 w-full rounded-lg outline-none" 
                        id="ingrediente" 
                        type="text"
                        placeholder="Nombre o ingrediente: Ej. Margarita, Vodka, Tequila, etc."
                        >
                </div>

                <div class="space-y-4 ">
                    <label  
                        class="block text-white uppercase font-extrabold text-lg" 
                        for="categoria">Categoria</label>
                    <select 
                        class="p-3 w-full rounded-lg outline-none" 
                        id="categoria" 
                        >
                        <option value="">--- SELECCIONE ---</option>
                    </select>
                </div>

                <input 
                    type="submit"
                    value="Buscar receta"
                    class="bg-orange-800 hover:bg-orange-900 cursor-pointer text-white font-extrabold w-full p-2 rounded-lg uppercase"
                    >
            </form>
        </div>
    </header>
</template>

