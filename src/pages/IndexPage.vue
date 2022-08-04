<template>
  <q-page class="column justify-evenly">
    <InputPesquisa />
    <CardObra />
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import InputPesquisa from 'src/components/InputPesquisa.vue'
import CardObra from 'src/components/CardObra.vue'

export default defineComponent({
  name: 'IndexPage',
  components: { InputPesquisa, CardObra }
})
</script>
