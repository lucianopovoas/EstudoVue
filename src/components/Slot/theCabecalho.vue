<template>
    <div class="cabecalho">
        
        <slot></slot>
        <h1>
            <slot name="titulo"></slot>
        </h1>
        <p v-if="$slots.descricao">
            <slot name="descricao"></slot>
        </p>
    </div>
</template>

<script>
export default {
    name: 'theCabecalho',
    mounted(){
        console.log(this.$slots)
    }
}
</script>

<style scoped>
    .cabecalho{
        background-color: black;
        color: white;
    }
</style>