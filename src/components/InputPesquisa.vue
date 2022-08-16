<template>
  <q-input
    class="input-search efeito-zoom"

    standout="bg-default text-white"
    style="background-color: white; border-radius: 4px"
    v-model="text"
    :dense="dense"
    placeholder="Digite o que deseja buscar..."
  >
    <template v-slot:append>
      <q-icon name="search" />
    </template>
  </q-input>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'InputPesquisa',
  setup () {
    return {
      text: ref(''),
      ph: ref(''),
      dense: ref(false)
    }
  }
})
</script>

<style scoped>
.input-search{
  width: 95%;
  max-width: 600px;
  margin: 0 auto;
}

</style>
