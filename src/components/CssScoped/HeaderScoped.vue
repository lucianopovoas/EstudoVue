<template>
    <ol>
        <li>Teste1</li>
        <li>Teste2</li>
        <li>Teste3</li>
    </ol>
</template>

<script>
    export default{
        name: 'HeaderScoped'
    }
</script>

<style scoped>
    ol{
        background-color: black;
    }
    li{
        color: yellow;
        font-size: large;
    }
    li:hover{
        color: orangered;
    }
</style>