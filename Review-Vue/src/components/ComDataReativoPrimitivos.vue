<template>
    <div class="component">
        <h1>Componente com Dados Reativos Primitivos</h1>
        <p>Nome: {{nome}} | Idade:{{idade}}</p>
        <!-- Tanto faz V-ON ou @ -->
        <button v-on:click="fazerAniversario">Fazer Aniversário</button>
        <button @click="mudarNome">Mudar Nome</button>
    </div>
</template>


<script setup>
    import {ref} from 'vue'
    const nome = ref("André")
    const idade = ref(26) 

    function fazerAniversario(){
        idade.value += 1
    }

    function mudarNome(){
        nome.value = "André Filipe"
    }
</script>