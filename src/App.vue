<script setup>
import { ref, onMounted } from "vue";
import { perguntas } from "./mocks/perguntas.js";

const frase = ref("")

function getAleatoriaFrase() {
    const tipo = Math.random() < 0.5? 'verdades' : 'desafios';
    const indice = Math.floor(Math.random() * perguntas[tipo].length);
    return perguntas[tipo][indice];
}

const girar = () => frase.value = getAleatoriaFrase()

onMounted(() => {
    frase.value = getAleatoriaFrase()
})
</script>

<template>
 <h1 class="poetsen ft-pink">Hot_challenges</h1>
 <p class="panel-text nanum ft-blue ft-22">{{ frase.pergunta }}</p>
 <p class="zeyada ft-blue ft-30 align-right">{{ frase.categoria }}</p>

 <button class="btn" @click="girar">Girar</button>
</template>
