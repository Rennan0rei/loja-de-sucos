<script setup>
import ListaDeSucos from './components/ListaDeSucos.vue';
</script>

<template>
  <div>
    <h1 class="titulo">Sucada Maravilhas</h1> <!-- Nome da loja aparece apenas uma vez -->
    <ListaDeSucos />
  </div>
</template>

<style scoped>
.titulo {
  text-align: center;
  font-size: 2em;
  color: #42b883; /* Cor verde típica do Vue, mude como quiser */
  margin-bottom: 20px;
}
</style>
