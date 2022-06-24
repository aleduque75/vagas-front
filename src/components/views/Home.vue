<template>
 <div class="container py-4">
  <div class="row">
    <div class="col">
      <pesquisar-vaga></pesquisar-vaga>
    </div>
  </div>

  <div class="row mt-5">
    <div class="col">
      <div class="card">
        <div class="card-header bg-dark text-white">Titulo da Vaga</div>
        <div class="card-body">
          <p>Descrição truncada da vaga</p>
        </div>
        <div class="card-footer">
          <small class="text-muted">Salário: R$ 6.000,00 | Modalidade: Home Officce | Tipo: CLT | Publicação: 10/11/2021</small>
        </div>
      </div>
    </div>
  </div>

  <div class="row mt-5">
    <div class="col-4">
      <indicador titulo="Vagas Abertas" indicador="100" bg="bg-dark" color="text-white" opa="bg-opacity-80"></indicador>

    </div>
    <div class="col-4">
    <indicador titulo="Proficionais Cadastrados" indicador="125" bg="bg-primary" color="text-white" opa="bg-opacity-60"></indicador>
    </div>

    <div class="col-4">
     <indicador titulo="Visitantes online" :indicador="usuariosOnline" bg="bg-warning" color="text-dark" opa="bg-opacity-60"></indicador>
    
    </div>

  </div>
 
 </div>
</template>

<script>

import PesquisarVaga from '../comuns/PesquisarVaga.vue'
import Indicador from '../comuns/Indicador.vue'

export default {
    name: 'HomE',
    components:{
      Indicador,      
      PesquisarVaga
    },
    data: () => ({
      usuariosOnline: 0
    }),
    methods: {
      getUsuariosOnline(){
        this.usuariosOnline = Math.floor(Math.random()*101)  // entre 0 e 100
      }
    },
    created() {
       setInterval(this.getUsuariosOnline, 1000) // a cada 1 segundo
    }
}

</script> 

<style module>
h1 {
  color:yellow;
}
</style>