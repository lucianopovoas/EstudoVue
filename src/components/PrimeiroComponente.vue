<template>
    <div>
        <h1>Olá vue!</h1>
        <h2>Olá {{nome}} {{ msg }}</h2>
    </div>
</template>

<script>
    export default{
        name:'PrimeiroComponente',
        data(){
            return{
                nome : "Matheus",
                msg : "Seja bem vindo"
            }
        }
    }
</script>

<style>
    .primeiroH1{
        background-color: blue;
    }
</style>
