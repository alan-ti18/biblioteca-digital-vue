<template>
  <div class="cards-container">
    <CardObra v-for="(card, index) in cards" :key="index" :card="card" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import CardObra from './CardObra.vue'

export default defineComponent({
  name: 'CardsContainer',
  data () {
    return {
      cards: [
        {
          anoPublicacao: 2018,
          ativa: true,
          autores: ['Fulano', 'Beltrano'],
          cadastradoPor: 'Fulaninho',
          categorias: ['ssp', 'teste'],
          dataDeCadastro: new Date(),
          sinopse: 'Testando isso aqui Testando isso aqui Testando isso aqui Testando isso aqui Testando isso aqui',
          tipo: 'revista',
          titulo: 'Testando Card'
        },
        {
          anoPublicacao: 2018,
          ativa: true,
          autores: ['Fulano', 'Beltrano'],
          cadastradoPor: 'Fulaninho',
          categorias: ['ssp', 'teste'],
          dataDeCadastro: new Date(),
          sinopse: 'Testando isso aqui Testando isso aqui Testando isso aqui Testando isso aqui Testando isso aqui',
          tipo: 'revista',
          titulo: 'Testando Card'
        }
      ]
    }
  },
  components: {
    CardObra
  }
})

</script>

<style>
.cards-container{
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 32px;
  margin: 80px auto;
  width: 95%;
  max-width: 1200px;
}

</style>
