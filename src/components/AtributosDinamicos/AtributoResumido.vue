<template>
    <img :src="avatar" :alt="descricao">
</template>

<script>
    export default{
        name: 'AtributoResumido',
        data(){
            return{
                avatar: "/img/avatar.png",
                descricao: "Avatar"
            }
        }
    }
</script>