<template>
    <button @click="onClick">X</button>
</template>

<script>
    export default {
        name: 'EmitDado',
        methods:{
            onClick(){
                    //Nome do evento
                    this.$emit('close')
                    console.log("click")
            }
        }
    }
</script>