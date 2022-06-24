<template>
        <div :class="estilo">
            <p>{{titulo}}</p>
            <h2>{{indicador}}</h2>
        </div>
</template>

<script>
export default {
    name: 'IndicadoR',
    props: ['titulo', 'indicador', 'bg', 'color', 'opa'],
    computed: {
        estilo(){
            return `h-5 p-3 rounded-3 border ${this.bg} ${this.color} ${this.opa}`
        }
    }
}
</script>