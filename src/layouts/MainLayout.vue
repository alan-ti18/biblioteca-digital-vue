<template>
  <q-layout view="hHh lpr fFf">
    <q-header elevated class="row">
      <q-toolbar class="justify-evenly">
        <q-avatar class="col-4">
          <img src="../assets/img/COGER_VETOR.9613c988.png" alt="Página Inicial" />
        </q-avatar>
        <q-toolbar-title class="text-h4">
          Biblioteca Digital COGER
        </q-toolbar-title>
        <q-btn no-caps class="q-px-lg q-py-sm text-subtitle1" color="transparencia" text-color="transparencia" label="Saiba mais sobre a Biblioteca Digital" />
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'MainLayout',
  components: { }
})
</script>
