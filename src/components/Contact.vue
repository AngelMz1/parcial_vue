<template>
    <div class="p-4 sm:ml-64">
        <div class="max-w-4xl mx-auto text-center">
            <form @submit.prevent="sendForm()">
                <fieldset class="border border-gray-300 rounded-lg p-6">
                    <legend class="text-2xl font-bold text-black px-4">Formulario con vue.js</legend>
                    <div class="mb-4">
                        <label for="name" class="block text-gray-700 font-bold mb-2">Nombre:</label>
                        <input type="text" id="name" v-model="informacion.nombre" class="border border-gray-300 rounded-lg px-4 py-2 w-full">
                    </div>
                    <div class="mb-4">
                        <label for="email" class="block text-gray-700 font-bold mb-2">Correo electrónico:</label>
                        <input type="email" id="email" v-model="informacion.email" class="border border-gray-300 rounded-lg px-4 py-2 w-full" required>
                    </div>
                    <div class="mb-4">
                        <label for="message" class="block text-gray-700 font-bold mb-2">Mensaje:</label>
                        <textarea id="message" v-model="informacion.message" class="border border-gray-300 rounded-lg px-4 py-2 w-full" required></textarea>
                    </div>
                    <div class="flex justify-center">
                        <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-lg" >Enviar</button>
                    </div>
                </fieldset>
            </form>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Contact',
    data() {
        return {
            informacion: {
                nombre: '',
                email: '',
                message: ''
            }
        }
    },
    methods: {
        sendForm() {
            console.log(this.informacion);
        }
    }
}
</script>
<style>

</style>