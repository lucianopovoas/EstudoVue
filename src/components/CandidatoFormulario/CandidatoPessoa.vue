<template>
    <div>
        <h1>Candidato: {{ nome }}</h1>
        <h3>Experiencia:</h3>
        <InfoCandidato />
    </div>
    <div>
        <FormCandidato />
    </div>
</template>

<script>
import FormCandidato from './FormCandidato.vue';
import InfoCandidato from './InfoCandidato.vue';

    export default{
        name: 'CandidatoPessoa',
        components:{
            InfoCandidato,
            FormCandidato
        },
        data(){
            return{
                nome: "Matheus"
            }
        }
    }
</script>