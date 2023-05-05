<template>
    <div class="citacao">
        <slot name="dev"></slot>
        <slot name="autor"></slot>
        <slot name="fonte"></slot>
        <slot name="texto"></slot>

    </div>
</template>

<script>

export default {
    created(){
        console.log("Aqui é onde o ciclo de vida cria meu componente")
    },
    destroyed(){
        console.log("Aqui é onde meu ciclo de vida destroi o componente")
    },
    activated(){
        console.log("Aqui ele vai mostrar que quando estiver nesse componente vai estar ativado --ATIVADO")
    },
    deactivated(){
        console.log("Aqui ele vai mostrar que o componente foi desativado, quando não estiver nele-- DESATIVADO")

    }
    
}
</script>

<style scoped>
    .citacao {
        border: 1px solid #DDD;
        background-color: rgba(0, 0, 0, .1);
        padding: 25px;
        max-width: 450px;
    }
</style>
