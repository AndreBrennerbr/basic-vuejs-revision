<template>
    <div class="component">
        <h1>Componente com data binding</h1>
        <p>{{valor}}</p>
        <!-- ONE WAY DATA BINDING <input type="text" v-bind:value="valor"></input> -->

        <!-- TWO WAY DATA BINDING -->
       <!--  <input type="text" :value="valor" @input="(e) => valor=e.target.value"></input> -->
       <!--  <input type="text" v-bind:value="valor" v-on:input="(e) => valor=e.target.value"></input> -->

       <input type="text" v-model="valor"></input>
        
    </div>
</template>

<script setup>
import {ref} from 'vue'
const valor = ref("Vue é muito legal")
</script>