<script setup>
import { ref } from "vue";
import { perguntas } from "./mocks/perguntas.js";

const verdades = ref(perguntas)
</script>

<template>
 <h1 class="poetsen ft-pink">Hot_challenges</h1>
 <p class="panel-text nanum ft-blue ft-22">{{ verdades.verdade[2].pergunta }}</p>
 <p class="zeyada ft-blue ft-30 align-right">verdade</p>
</template>
