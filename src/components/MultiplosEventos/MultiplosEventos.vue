<template>
    <button @click="primeiro($event), segundo('Segundo Evento Ativado', $event), terceiro(txt2, $event)">Ativar Multiplos Eventos</button>
    <p>{{ exemplo }}</p>
</template>

<script>
    export default{
        name: 'MultiplosEventos',
        data() {
            return{
                exemplo: "",
                txt2: "Terceiro Evento Ativado"
            }
        },
        methods:{
            primeiro(e){
                this.exemplo = "Primeiro Evendo Ativado"
                e.preventDefault()
            },
            segundo(txt, e){
                setTimeout(() => {
                    this.exemplo = txt    
                }, 1000);
                e.preventDefault()
            },
            terceiro(txt2, e){
                setTimeout(() => {
                    this.exemplo = txt2   
                }, 2000);
                e.preventDefault()
            }
        }    
    }
</script>
