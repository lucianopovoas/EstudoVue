<template>
    <p>Para acessar o site <a v-bind:href="meuLink">Clique aqui</a></p>
</template>

<script>
    export default{
        name: 'AtributoVBind',
        data(){
            return{
                meuLink: 'https://google.com'
            }
        }
    }
</script>