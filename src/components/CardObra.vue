<template>
  <div>
    {{ obras }}
  </div>
  <div class="grid-card">
    <img src="../assets/img/capa-teste.jpeg" alt="capa" class="capa">
    <h4 class="titulo">{{ card.titulo }}</h4>
    <p class="autor" v-for="(autor, index) in card.autores" :key="index">
      {{ autor }}
    </p>
    <p class="ano-publicacao">{{ card.anoPublicacao }}</p>
    <span class="categorias" v-for="(categoria, index) in card.categorias" :key="index">
      {{ categoria }},
    </span>
    <span class="tipo">{{ card.tipo }}</span>
    <p class="sinopse">{{ card.sinopse }}</p>

  </div>

</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import { api } from '../boot/axios'

export default defineComponent({
  name: 'CardObra',
  setup () {
    return {
      stars: ref(4),
      obras: null
    }
  },
  props: ['card'],
  methods: {
    listarObras () {
      api.get('/obras')
        .then((res) => {
          this.obras = res.data
        })
    }
  },
  created () {
    console.log('começando..')
    this.listarObras()
  }
})
</script>

<style scoped>
.my-card{
  width: 100%;
  max-width: 300px;
}

p{
  margin: 0;
}

.grid-card{
  background-color: #efefef;
  border-radius: 8px;
  box-shadow: 0 0 15px rgba(44, 44, 44, .2);
  width: 100%;
  min-width: 200px;
  padding: 16px;
  display: grid;
  grid-template-columns: 200px 1fr 1fr;
  gap: 8px;
  grid-template-areas:
    "capa     titulo          titulo"
    "capa     autor           autor"
    "capa     ano-publicacao  ano-publicacao"
    "capa     categoria       categoria"
    "capa     .               tipo"
    "sinopse  sinopse         sinopse"
  ;
  }
  .grid-card img{
    display: grid;
    max-height: 200px;
    width: auto;
  }

.capa {
  grid-area: capa;
}
.titulo {
  grid-area: titulo;
  margin: 0;
}
.autor{
  grid-area: autor;
}
.ano-publicacao{
  grid-area: ano-publicacao;
  margin: 0;
}
.categorias{
  grid-area: categoria;
}
.tipo{
  grid-area: tipo;
  justify-self: end;
  background-color: #456789;
  position: relative;
  right: -16px;
  padding: 8px 16px;
  border-radius: 8px 0 0 8px;
  color: white;
}
.sinopse{
  grid-area: sinopse;
}
</style>
