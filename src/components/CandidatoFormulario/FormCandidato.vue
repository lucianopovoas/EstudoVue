<template>
    <Form>
        <InputText />
        <InputText />
        <input type="submit" value="Enviar">
    </Form>
</template>

<script>
import InputText from './InputText.vue';

    export default{
        name: 'FormCandidato',
        components: {
            InputText
        }
    }
</script>