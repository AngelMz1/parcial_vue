<template>
  <div class="p-4 sm:ml-64">
    <div class="max-w-4xl mx-auto text-center">
      <h1 class="text-3xl font-bold text-black mb-6">Componente Padre</h1>
      <div v-for="animal in animales" v-bind:key="animal.nombre" class="mb-4">
        <ComponentSon :animal="animal" v-on:compartir="compartir"/>
      </div>
    </div>
  </div>
  <hr class="my-8">
  <div v-if="animalfav" class="p-4 sm:ml-64">
    <div class="max-w-4xl mx-auto text-center">
      <h1 class="text-3xl font-bold text-black mb-6">Animal Favorito: {{ animalfav.nombre }}</h1>
      <p class="text-black text-lg">{{ animalfav.tamaño }}, {{ animalfav.peso }}, {{ animalfav.habitat }}</p>
    </div>
  </div>
</template>

<script>
import ComponentSon from './ComponentSon.vue';

export default {
    name: 'ComponentFather',
    components: {
        ComponentSon
    },
    methods:{
        compartir(compartir){
            this.animalfav = compartir;
        }
    },
    data() {
        return {
            animalfav: null,
            animales: [
                { nombre: 'León', tamaño: 'Grande', peso: '190 kg', habitat: 'Sabana africana' },
                { nombre: 'Pingüino', tamaño: 'Mediano', peso: '25 kg', habitat: 'Antártida' },
                { nombre: 'Colibrí', tamaño: 'Pequeño', peso: '4 g', habitat: 'Bosques tropicales' },
                { nombre: 'Elefante', tamaño: 'Muy grande', peso: '6000 kg', habitat: 'Sabana y bosques' },
                { nombre: 'Delfín', tamaño: 'Grande', peso: '150 kg', habitat: 'Océanos' }
            ]
        }
    }
}
</script>

<style scoped>
/* Estilos específicos del componente */
</style>
