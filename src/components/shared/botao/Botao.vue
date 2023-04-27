<template>

    <button @click="disparaAcao()" class="button danger-button normal-button">{{ rotulo }}</button>

</template>

<script>

    export default {

        props: ['tipo', 'rotulo'],

        methods: {

            disparaAcao() {
                if(confirm('Confirma operação?')) {
                    this.$emit('botaoAtivado');
                }
            }
        }
    }

</script>


<style>

    .button {
        display: inline-block;
        padding: 10px;
        border-radius: 3px;
        margin: 10px;
        font-size: 1.2rem;
    }
    
    .danger-button {
        background-color: firebrick;
        color: white;
    }

    .normal-button {
        background-color: darkcyan;
        color: white;
    }

</style>