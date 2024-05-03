<template>
    <button @click="mostrarEmail">{{ frase }}</button>
    <p v-if="mostrar">{{ email }}</p>
</template>

<script>
    export default{
        name: 'MetodosVue',
        data(){
            return{
                frase: "Mostrar Email",
                email: "exemplo@gmail.com",
                mostrar: false
            }
        },
        methods: {
            mostrarEmail(){
                this.mostrar = !this.mostrar
                if(this.frase == "Mostrar Email"){
                    this.frase = "Esconder Email"
                }else{
                    this.frase = "Mostrar Email"
                }
            }
        }
    }
</script>