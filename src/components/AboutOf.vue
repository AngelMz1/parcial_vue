<template>
    <div class="p-4 sm:ml-64">
        <div class="max-w-4xl mx-auto text-center">
            <h3 class="text-3xl font-bold text-black mb-6">Anime: Dandadan</h3>
            <p class="text-black text-lg leading-relaxed">Dandadan o Dan Da Dan (ダンダダン?) es una serie de manga japonés escrita e ilustrada por Yukinobu Tatsu. Se publica en la aplicación y web Shōnen Jump+ de Shūeisha desde el 6 de abril de 2021. Shūeisha también publica sus entregas en la web y app Manga Plus en español e inglés. Una adaptación a serie anime de televisión producida por Science Saru se estrenó el 4 de octubre de 2024.</p>
        </div>
        <div class="max-w-4xl mx-auto text-center mt-8">
            <button @click="redireccion()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Ver en crunchyroll</button>
        </div>
        <div class="max-w-4xl mx-auto text-center mt-4">
            <button @click="peticion" class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded">Realizar petición</button>
        </div>
    </div>
</template>
<script>
import axios from 'axios';
export default {
    name: 'AboutOf',
    methods: {
        redireccion() {
            window.open('https://www.crunchyroll.com/es/series/GG5H5XQ0D/dan-da-dan?srsltid=AfmBOor4oYh8y2xclM1hwBO0aH39Lf9nEYFs-CYVXXAcKj6pR2dG8eS8', '_blank');
        },
        peticion() {
            axios.get('https://randomuser.me/api/')
                .then(response => {
                    console.log(response.data);
                })
                .catch(error => {
                    console.error('Error en la petición:', error);
                }); 
        }
    }
}

</script>
<style>

</style>