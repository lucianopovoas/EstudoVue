<template>
    <div :class="baseClass">
        Formulário Enviado com Sucesso!
    </div>
</template>

<script>
    export default{
        name: 'PropsDado',
        props:{
            variante:{
                type: String,
                default: ''
            }
        },
        computed:{
            baseClass(){
                return [
                    'alert',
                    this.variante ? `alert-${this.variante}` : ''
                ]
            }
        },
    }
</script>

<style scoped>
    .alert{
        background: gray;
        width: 230px;
        padding: 5px;
        border-radius: 5px;
    }
    .alert-error{
        background-color: red;
    }
    .alert-success{
        background: green;
    }
</style>
