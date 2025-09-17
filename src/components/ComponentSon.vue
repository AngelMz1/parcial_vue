<template>
  <div>
    <!-- Contenido del template -->
     <h4>{{ animal.nombre }}</h4>
     <p>{{ animal.tamaño }}, {{ animal.peso }}, {{ animal.habitat}}</p>
     <button @click="compartir(animal)" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Compartir</button>
  </div>
</template>
<script>
export default {
    name: 'ComponentSon',
    props: ['animal'],
    methods: {
        compartir(animal) {
            this.$emit('compartir', animal);
        }
    }
}
</script>

<style scoped>
/* Estilos específicos del componente */
</style>
