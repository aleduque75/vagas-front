<template>
 <div>
  <h1>{{titulo}}</h1>
<button @click="atualizarComponente()">Atualizar</button>
<button @click="conteudo = 'home'">Home</button>
<button @click="conteudo = 'publicar-vaga'">Publicar Vaga</button>
  <!-- renderizar de modo dinamico os componentes home e publicar vaga -->
  <!-- <home></home> -->
  <!-- <publicar-vaga></publicar-vaga> -->
 <keep-alive>
 <component :is="conteudo"></component>
 </keep-alive>

 </div>
</template>

<script>
import Home from '@/components/views/Home.vue'
import PublicarVaga from '@/components/views/PublicarVaga.vue'
export default {
    name: 'ConteudoPadrao',
    components: {
        Home,
        PublicarVaga
    },
    data:()=> ({
        teste: 'O componetne foi criado',
        titulo: 'Componente Conteudo',
        conteudo: 'home'
    }),
    methods: {
        atualizarComponente(){
            this.titulo += '*'
        }
    },
    // beforeCreate() {
    //     console.log('Antes de Criar', this.teste)
    // },
    // created() {
    //     console.log('Criado', this.teste)
    // },
    // beforeMount() {
    //     console.log('Antes de montar o template')
    // },
    // mounted() {
    //      console.log('Montado')
    // },
    // beforeUpdate() {
    //     console.log('Antes de atualizar')
    // },
    // updated() {
    //     console.log('Atualizado')
    // },
    // beforeUnmount() {
    //     console.log('Antes de desmontar/destruir')
    // },
    // unmounted() {
    //     console.log('Desmontado/destruido')
    // },
    // errorCaptured(){
    //     console.log('Erro capturado')
    // },
    // renderTracked() {
    //     console.log('Re-renderização restreada')
    // },
    // renderTriggered() {
    //     console.log('Re-renderização ativada')
    // },
    // activated() {
    //     console.log('Componente Ativado')
    // },
    // deactivated() {
    //     console.log('Componente desativado')
    // },

}


</script>

<style module>
.teste-1{
    background-color: red;
}
#teste-2 {
    background-color: yellow;
}

h1 {
  color: aquamarine;
}
</style>