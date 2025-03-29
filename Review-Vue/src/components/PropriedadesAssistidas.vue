<!-- 
São variaveis que dependem de outras variaveis, que vão ser atualizadas
quando outras variaveis mudarem - Quando a gente precisa de um efeito colateral 
a partir de uma mudança - exemplo : mudar a dom, req pra api externa, tudo isso além de
mudar o valor
-->

<template>
    <div class="component">
        <h1>Componente com Propriedades Assistidas</h1>
        <p> Idade: {{ idade }}</p>
        <label>Ano Nascimento:</label>
        <input type="number" v-model="anoNascimento" min="1900">
        <label>Ano Atual:</label>
        <input type="number" v-model="anoAtual" min="2000">
    </div>
</template>

<script setup>
import { ref } from 'vue';
/* import {watch} from 'vue'; */
import {watchEffect} from 'vue'; 
/* Diff : Sintaxe */


const anoNascimento = ref(1900)
const anoAtual = ref(2000)
const idade = ref(0)

/* watch(anoAtual, (ano) => {
    idade.value = ano - anoNascimento.value
})

watch(anoNascimento, (ano) => {
    idade.value = anoAtual.value - ano
}) */

watchEffect(() => {
    idade.value = anoAtual.value - anoNascimento.value
})

</script>

<style scoped>
label{
    margin: 10px;
}
</style>