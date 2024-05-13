<template>

    <div class="custom">
        <p>{{ fullNome }}</p>

        <h2>Cadastrados</h2>

        <div v-for="todo in cadastradoTodos" :key="todo.nickId">
            {{ todo.tittle }} <span>{{ todo.cadastrado }}</span>
        </div>

        <h2>Não Cadastrados</h2>

        <div v-for="todo in naoCadastradoTodos" :key="todo.nickId">
            {{ todo.tittle }} <span>{{ todo.cadastrado }}</span>
        </div>
    </div>

</template>

<script>
    export default {
        name: 'ComputedPropriedade',
        data(){
            return{
                user:{
                    primeiroNome: 'XXX',
                    ultimoNome: 'YYY'
                },
                todos:[
                    {
                        "nickId": 1,
                        "tittle": "aaaaaaa",
                        "cadastrado": false
                    },
                    {
                        "nickId": 2,
                        "tittle": "bbbbb",
                        "cadastrado": true
                    },
                    {
                        "nickId": 3,
                        "tittle": "ccccccc",
                        "cadastrado": true
                    }
                ]
            }
        },
        computed:{
            fullNome(){
                return `${this.user.primeiroNome} ${this.user.ultimoNome}`
            },
            cadastradoTodos(){
                return this.todos.filter(todo => todo.cadastrado)
            },
            naoCadastradoTodos(){
                return this.todos.filter(todo => !todo.cadastrado)
            }
        }
    }
</script>

<style scoped>
    .custom{
        color: yellow;
    }
</style>