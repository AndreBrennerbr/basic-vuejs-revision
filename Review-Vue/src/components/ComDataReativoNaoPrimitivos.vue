<template>
    <div class="component">
        <h1>Componente com Dados Reativos Não Primitivos</h1>
        <p>Nome: {{pessoa.nome}} | Idade:{{pessoa.idade}}</p>
        
        <button @:click="fazerAniversario">Fazer Aniversário</button>
        <button @click="mudarNome">Mudar Nome</button>
    </div>
</template>


<!-- <script setup>
    import {reactive} from 'vue'
    const pessoa  = reactive({nome : "Lucas", idade : 30})
 

    function fazerAniversario(){
        pessoa.idade += 1
    }

    function mudarNome(){
        pessoa.nome = "Filipe"
    }
</script> -->

<script>
    export default{
        data:function(){
            return{
                pessoa:{
                    nome : "Lucas",
                    idade : 30
                }
            }
        },
        methods:{
            fazerAniversario:function(){
                this.pessoa.idade += 1
            },
            mudarNome:function(){
                this.pessoa.nome = "Luiz"
            }
        }
    }
</script>