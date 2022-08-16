<template>
  <q-page class="column q-mt-xl">
    <InputPesquisa />
    <CardsContainer />
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import InputPesquisa from 'src/components/InputPesquisa.vue'
import CardsContainer from 'src/components/CardsContainer.vue'

export default defineComponent({
  name: 'IndexPage',
  components: { InputPesquisa, CardsContainer }
})
</script>
