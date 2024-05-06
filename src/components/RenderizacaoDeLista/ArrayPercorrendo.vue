<template>
    <ul>
        <li v-for="(nome, index) in nomes" v-bind:key="index">{{ nome }}</li>
    </ul>
    <ol>
        <li v-for="integrante in cadastrados" v-bind:key="integrante.id"> {{ integrante.idade }} Anos, Idioma: {{ integrante.Linguagem }}</li>
    </ol>
</template>

<script>
    export default{
        name:'ArrayPercorrendo',
        data(){
            return{
                nomes: ["Pedro", "Maria", "Jose"],
                cadastrados: [
                    {id: 1, Linguagem: "Português", idade: 30},
                    {id: 2, Linguagem: "Português", idade: 25},
                    {id: 3, Linguagem: "Espanhol", idade: 22},
                ]
            }
        }
    }
</script>