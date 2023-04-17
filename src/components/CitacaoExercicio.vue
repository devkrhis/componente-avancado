<template>
    <!-- Dessa forma é a classica vai puxar tudo o que está definido dentro de citacao no slot
    <div class="citacao">
        <slot></slot>
    </div>
        
    --> 
    <!-- Multiplos Slots -->
    <div class="citacao">
        <slot name="fonte"></slot>
        <slot name="texto"></slot>
        <slot name="autor"></slot>
    </div>
</template>

<script>

export default {

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
