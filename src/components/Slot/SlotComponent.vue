<template>
    <div>
        <!-- Padrão -->
        <theCabecalho>
        <div>Padrão</div>
        <template v-slot:titulo>Titulo</template>
        </theCabecalho>
        
    </div>
</template>

<script>
import theCabecalho from './theCabecalho.vue'

    export default {
        name: 'SlotComponent',
        components:{
            theCabecalho
        },
    }
</script>