<!-- São formas de passar inf do comp pai para o filho, semelhante a props
Só que os slots servem para passar HTML ou componentes para dentro do componente
-->

<template>
    <div class="component">
        <h1>Componente com Slots</h1>
        <button> 
            <slot name="icone"/> 
            <slot name="texto">
            <!-- Se fizer dessa forma se define o valor padrão aqui, caso não seja passado valor no slot -->
             Botão
            </slot>
        </button>
    </div> 
</template>