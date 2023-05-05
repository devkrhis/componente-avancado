<template>
    <div class="citacoes">
        <span>
            <button @click="numero--">&lt;</button>
            <button @click="numero++">&gt;</button>
        </span>
        <CitacaoExercicio>
            <p slot="texto"> {{ citacoes[indice].texto }}</p>
            <p slot="autor"> {{ citacoes[indice].autor }}</p>
            <p slot="fonte"> {{ citacoes[indice].fonte }}</p>
            <p slot="dev"> {{ citacoes[indice].dev }}</p>

        </CitacaoExercicio>
    </div>
</template>
<script>
import CitacaoExercicio from './CitacaoExercicio.vue';

export default {
    components : { CitacaoExercicio },
    data() {
        return {
            numero: 0,
            citacoes: [{
                fonte: 'Jornal do Empreendedor',
                texto: 'Lembre-se sempre que você é absolutamente único. Assim como todos os outros.',
                autor: 'Margaret Mead',
                dev: 'Krhistopher'
            }, { 
                fonte: 'Frases de Mãe',
                texto: 'Isso não é um quarto, é um chiqueiro.',
                autor: 'Roberta',
                dev: 'Krhistopher'
            }, {
                fonte: 'Frases de Pai',
                texto: 'Vou contar até 3! 1, 2, 2...',
                autor: 'Gustavo',
                dev: 'Krhistopher'
            }]
        }
    },
    computed: {
        indice() {
            return Math.abs(this.numero % 3)
        }
    }
}
</script>

<style scoped>
    .citacoes {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .limitText p{
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
    }
</style>
