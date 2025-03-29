<script setup>
  import Componente from './components/Componente.vue'
  import ComData from './components/ComData.vue'
  import ComDataReativoPrimitivos from './components/ComDataReativoPrimitivos.vue';
  import ComDataReativoNaoPrimitivos from './components/ComDataReativoNaoPrimitivos.vue';
  import DataBinding from './components/DataBinding.vue';
  import ComProps from './components/ComProps.vue';
  import EscutaEvento from './components/EscutaEvento.vue';
  import PropriedadesComputadas from './components/PropriedadesComputadas.vue';
  import PropriedadesAssistidas from './components/PropriedadesAssistidas.vue';
  import RederizacaoCondiciona from './components/RederizacaoCondiciona.vue';
  import RederizacaoListas from './components/RederizacaoListas.vue';
  import Slots from './components/Slots.vue'
  
  const borracha="Borracha"
  const precoBorracha = 2.50

  const CachorrosBrenner = [
    {nome:"Luke",idade:3},
    {nome:"Crowley",idade:4},
    {nome:"Achad",idade:5},
  ]

</script>

<template>
  <header>Vue</header>
  <Slots>
    <template v-slot:icone>
      <svg  
          xmlns="http://www.w3.org/2000/svg"  
          width="24"  
          height="24"  
          viewBox="0 0 24 24"  
          fill="none"  
          stroke="currentColor"  
          stroke-width="2"  
          stroke-linecap="round" 
          stroke-linejoin="round"  
          class="icon icon-tabler icons-tabler-outline icon-tabler-home">
          <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
          <path d="M5 12l-2 0l9 -9l9 9l-2 0" />
          <path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7" />
          <path d="M9 21v-6a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v6" />
      </svg>
    </template>
    <template v-slot:texto>
      Home
    </template>
  </Slots>
  <RederizacaoListas nome="Brenner" :cachorros="CachorrosBrenner"/>
  <RederizacaoCondiciona nome="André Brenner" :qtde-cachorros="1"/>
  <PropriedadesAssistidas/>
  <PropriedadesComputadas/>
  <EscutaEvento/>
  <ComProps :item="borracha" :preco="precoBorracha"/>
  <DataBinding/>
  <ComDataReativoPrimitivos/>
  <ComDataReativoNaoPrimitivos/>
  <ComData/>
  <Componente/>
</template>

<style scoped>

</style>
