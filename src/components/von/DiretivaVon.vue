<template>
    <button v-on:click="clicou">Botão</button>
    <button @click="clicou">Botão2</button>
    <div @mouseover="entrou">Mouse</div>
    <input type="text" @keydown.space="apertou">
</template>

<script>
    export default {
        name: 'DiretivaVon',
        data(){
            return{

            }
        },
        methods:{
            clicou(){
                alert("Clicado")
            },
            entrou(){
                alert("entrou")
            },
            apertou(){
                alert("Apertou Espaço, Pular")
            }
        }
    }
</script>