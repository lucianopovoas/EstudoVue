<template>
    <div>
        <h1>Cidade: {{ cidade }}</h1>
        <theHeader v-if="showHeader" />
        <button @click="showHeader = !showHeader">Ativar e Desativar</button>
    </div>
</template>

<script>
import theHeader from './theHeader.vue'

    export default{
        name: 'LifeCicleHook',
        data(){
            return{
                cidade: "Salvador" ,
                showHeader: false  
            }
        },
        components: {
            theHeader
        },
        //Antes de ser Criado
        beforeCreate(){
            console.log("BeforeCreate")
            console.log('Estado: ', this.cidade)
            console.log('Dom:', this.$el);
        },
        //Criado
        created(){
            console.log("Create")
            console.log('Estado: ', this.cidade)
            console.log('Dom:', this.$el);
        },
        //Antes de ser montado
        beforeMount(){
            console.log("BeforeMount")
            console.log('Estado: ', this.cidade)
            console.log('Dom:', this.$el);
        },
        //Montado
        mounted() {
            console.log("Mounted")
            console.log('Estado: ', this.cidade)
            console.log('Dom:', this.$el);
        },
        //Antes de ser desmontado
        beforeUnmount(){
            console.log("BeforeUnmount")
            console.log('Estado: ', this.cidade)
            console.log('Dom:', this.$el);
        },
        //Desmontado
        unmounted(){
            console.log("Unmounted")
            console.log('Estado: ', this.cidade)
            console.log('Dom:', this.$el);
        }
    }
</script>