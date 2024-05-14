<template>
    <h1>The Header</h1>
</template>

<script>
export default {
    name: 'theHeader',
    //Antes de ser desmontado
    beforeUnmount(){
        //Destruir
        console.log("beforeUnmount")
    },
    //Desmontado
    unmounted(){
        console.log("unmounted")
    }
}
</script>

<style scoped>
    h1{
        background-color: black;
        color: white;
    }
</style>