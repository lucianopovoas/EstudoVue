<template>
    <img :src="avatar" :alt="descricao">
</template>

<script>
    export default{
        name: 'DiretivaVBindResumido',
        data(){
            return{
                avatar: "/img/avatar.png",
                descricao: "Avatar"
            }
        }
    }
</script>