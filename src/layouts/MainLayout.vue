<template>
  <q-layout view="hHh lpr fFf">
    <q-header elevated class="row items-center">
      <q-toolbar>
        <img src="../assets/img/COGER_VETOR.9613c988.png" class="logo-img efeito-zoom"/>
        <q-toolbar-title class="text-h4" style="justify-self: center">
          Biblioteca Digital COGER
        </q-toolbar-title>
        <div class="btn-wrapper">
          <q-btn no-caps class="q-px-lg q-py-sm text-subtitle1 efeito-zoom" color="transparencia" text-color="default" label="Saiba mais sobre a Biblioteca Digital" />
        </div>
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

<style scoped>
  header.q-header{
    background: rgba(255, 255, 255, .35);
    height: 100px;
  }

  header .q-toolbar{
    height: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
  }

  header .q-toolbar .logo-img{
    height: 80%;
    max-height: 80px;
    margin-left: 20px;
    cursor: pointer;
  }

  div.text-h4{
    color: #426180 !important;
    font-weight: 500;
    line-height: normal;
  }

  .btn-wrapper{
    justify-self: flex-end;
  }

  button.q-btn{
    max-width: 350px;
    margin-right: 20px;
  }
</style>
