<template>
    <h3 v-if="estaTrabalhando">Parabéns pelo Cargo</h3>
    <h3 v-else>Cargo Disponivel</h3>

    <h3 v-show="mostrarNome">{{ nome }}</h3>
</template>

<script>
    export default{
        name: 'CadastroPessoa',
        data(){
            return{
                estaTrabalhando: true,
                mostrarNome: true,
                nome: "Luciano"
            }
        }
    }
</script>