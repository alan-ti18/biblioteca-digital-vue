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
.text-transparencia {
  color: #333 !important;
}
.bg-transparencia {
  background: rgba(255, 255, 255, .9) !important;
}
</style>
