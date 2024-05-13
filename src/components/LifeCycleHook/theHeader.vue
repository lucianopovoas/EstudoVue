<template>
    <h1>The Header</h1>
</template>

<script>
export default {
    name: 'theHeader',
    beforeUnmount(){
        //Destruir
        console.log("beforeUnmount")
    },
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