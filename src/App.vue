<template>
  <router-view />
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App'
})
</script>

<style>
*{
  font-family: 'Poppins', sans-serif;
}

body{
  background: url("./assets/img/bg-home.jpeg") no-repeat;
  background-size: cover;
  background-position: top left;
}

.text-transparencia {
  color: #333 !important;
}
.bg-transparencia {
  background: rgba(255, 255, 255, .7) !important;
}

.text-default {
  color: #426180 !important;
}

.bg-default {
  background: #426180 !important;
}

.efeito-zoom{
  transition: .2s;
}

.efeito-zoom:hover{
  transform: scale(1.05);
}
</style>
