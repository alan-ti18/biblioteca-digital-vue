<template>
  <q-input outlined v-model="text" :dense="dense">
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

<style>

</style>
