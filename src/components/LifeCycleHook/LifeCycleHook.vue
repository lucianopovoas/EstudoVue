<template>
    <h1>Cidade: {{ cidade }}</h1>
</template>

<script>
    export default{
        name: 'LifeCicleHook',
        data(){
            return{
                cidade: "Salvador"   
            }
        },
        created(){
            setTimeout(() => {
                this.cidade = "Feira de Santana"
            }, 1000);
        },
        mounted() {
            setTimeout(() => {
                this.cidade = "São Paulo"
            }, 2000);
        }
    }
</script>