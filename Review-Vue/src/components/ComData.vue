<template>
    <div>
        <h1>Componente com Dados</h1>
        <p>Nome: {{ nome }} - {{codigoProduto}}</p>
    </div>



</template>




<style scoped>
    div{
        text-align:center;
        border:2px solid rgb(10,69,4);
        background-color: #050b04;
        border-radius: 15px;
        margin:30px;
        padding:10px;

    }

    p{
        font-size: 1.2rem;
    }
</style>

<script setup>
    const nome = "Apontador";
    const codigoProduto = "#700";
</script>

<!-- <script>
//options api - Mais antiga
/* export default{
    data:function(){
        return{
            nome:"Caderno",
            codigoProduto:"#123"
        }
    }
} */

//Composition api - nova, porém a versão do setup é mais comum
/* export default{
    setup:function(){
        const nome = "Lápis";
        const codigoProduto = "#203";

        return{
            nome,
            codigoProduto
        }
    }
} */
</script> -->