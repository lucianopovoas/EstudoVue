<template>
    <button @click="clicou">Click</button>
    <form action="" @submit="enviarFormulario($event)">
        <input type="text" v-model="sobrenome">
        <input type="submit">
    </form>
</template>

<script>
    export default{
        name: 'EventosVue',
        data() {
            return{
                sobrenome: "Exemplo"
            }
        },
        methods:{
            enviarFormulario(e){
                e.preventDefault()

                const sobrenome = this.sobrenome

                alert(sobrenome)
            },
            clicou(){
                alert("Clicado")
            }
        }
    }
</script>
