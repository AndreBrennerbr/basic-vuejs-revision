<template>
    <div class="component">
        <h1>Componente que escuta evento</h1>
        <p>Total: R${{ total }}</p>
        <div class="lista">
            <EmiteEvento item="Item1" :preco="1.89" @FoiAdicionado="atualizarTotal"/>
            <EmiteEvento item="Item2" :preco="5" @FoiAdicionado="atualizarTotal"/>
            <EmiteEvento item="Item3" :preco="12" @FoiAdicionado="atualizarTotal"/>
        </div>
    </div>
</template>

<script setup>
import EmiteEvento from './EmiteEvento.vue';
import {ref} from 'vue'

const total = ref(0)

function atualizarTotal(preco){
    const valor = total.value + preco
    total.value = +valor.toFixed(2)
}


</script>

<style scoped>
.lista{
    display: flex;
    justify-content: space-between;
}

</style>