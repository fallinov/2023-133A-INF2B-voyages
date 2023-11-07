<script setup>
import {reactive, ref} from "vue";

// Création des données du composant
let annee = ref(2023); // ref() pour une donnée simple
const fruits = reactive(["pomme", "poire", "banane"]); // reactive() pour un objet
</script>

<template>
  <ul>
    <li v-for="fruit in fruits" :key="fruit">{{ fruit }}</li>
  </ul>
  <p>
    <slot></slot>
    - {{ annee }}
  </p>
</template>

<style scoped>
p {
  background-color: yellow;
  text-transform: uppercase;
}
</style>
