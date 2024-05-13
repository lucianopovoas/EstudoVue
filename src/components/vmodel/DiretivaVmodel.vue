<template>
    <div>
        <input type="text" v-model="name">
        <p>{{ name }}</p>

        <select v-model="esportes">
            <option value="">Escolha</option>
            <option value="futebol">futebol</option>
            <option value="skate">skate</option>
            <option value="tenis">tenis</option>
        </select>
        <p>{{ esportes }}</p>

        <input v-model="alternativa" type="radio" value="Sim"> Sim
        <input v-model="alternativa" type="radio" value="Não"> Não
        <p>{{ alternativa }}</p>

        <input v-model="termos" type="checkbox">Aceitar Termos 
        <p>{{ termos }}</p>

        <input v-model="cores" type="checkbox" value="Azul">Azul
        <input v-model="cores" type="checkbox" value="Amarelo">Amarelo
        <p>{{ cores }}</p>
    </div>
</template>

<script>
    export default{
        name: 'DiretivaVmodel',
        data(){
            return{
                name: '',
                esportes: '',
                alternativa: 'Sim',
                termos: true,
                cores: []
            }
        }
    }
</script>
