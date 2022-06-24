<template>
  <div>
    <h1> Texto na APP.vue</h1>
    <button @click="desmontarComponeten()">Desmontar o componente conteudo</button>
   <topo-padrao/>
    <conteudo v-if="visibilidade"></conteudo> 
  </div>
</template>

<script>
import Conteudo from '@/components/layouts/Conteudo.vue'
import TopoPadrao from '@/components/layouts/TopoPadrao.vue'

export default {
  name: 'App',
  data: () => ({
    visibilidade: true
  }),
  methods: {
    desmontarComponeten(){
      this.visibilidade = false
    }
  },
  components: {
    Conteudo,
    TopoPadrao
  }
}
</script>

<style module>

h1 {
  color: rgb(77, 67, 67);
}
</style>>
