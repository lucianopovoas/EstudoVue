<template>
    <br>
    <input v-model="nome" type="text">
    {{ nome }}

    <select v-model="count">
        <option value="5">5</option>
        <option value="10">10</option>
        <option value="15">15</option>
    </select>
    {{ count }}

    <input type="text" v-model="user.nick">
    <input type="text" v-model="user.password">
    {{ user.nick }} {{ user.password }}
</template>

<script>
    export default {
        name: 'WatchObservadores',
        data(){
            return{
                nome: '',
                count: 5,
                user: {
                    nick: '',
                    password: '',
                },
            }
        },
        watch:{
            nome(valor){
                if (valor.length >= 3){
                    this.saveUserName()
                }
            },
            count(){
                this.contador();
            },
            user:{
                handler(){
                    console.log("User alterado")
                },
                deep: true
            }
        },
        methods:{
            saveUserName(){
                console.log(this.nome)
            },
            contador(){
                console.log("Mudou Páginas")
            }
        }
    }
</script>