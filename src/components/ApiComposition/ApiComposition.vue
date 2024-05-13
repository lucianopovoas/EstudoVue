<template>
    <hr>

    <h1>Utilizando API COMPOSITION</h1>

    <h3 @click="MudarNome">{{nome}}</h3>
    <h3 @click="MudarNomeReativo">{{ user.primeiroNome }}</h3>
    <h3 @click="MudarNickReativo">{{ player.nick }}</h3>
</template>

<script>
import {ref, reactive } from 'vue'

    export default {
        name:'ApiComposition',
        setup(){

            //Não Reativo

            let nome = 'Nao Reativo'

            const MudarNome = () => {
                alert("Chegou")
                nome = 'Nao Funcionou'
            }

            //Forma 1 Reativo REACTIVE

            const user = reactive({
                primeiroNome: 'Reativo'
            })

            const MudarNomeReativo = () => {
                alert("Chegou Foi")
                user.primeiroNome = 'Funcionou'
            }

            //Forma 2 Reativo REF

            const player = ref({
                nick: 'Reativo'
            })

            const MudarNickReativo = () => {
                alert("Chegou Foi")
                player.value.nick = 'Funcionou'
            }

            return{
                nome,
                MudarNome,
                user,
                MudarNomeReativo,
                player,
                MudarNickReativo
            }
        }
    }
</script>