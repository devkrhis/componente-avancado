<template>
	<div id="app">
		<span>
			<button @click="componente = 'CitacoesExercicios' ">Citações</button>
			<button @click="componente = 'SobreExercicio' ">Sobre</button>
		</span>
		<keep-alive>
			<component :is="componente"/> <!-- Dessa forma ele resolve o nome da variavel exemplo:
			componente está recebendo ali em baixo CitacoesExercicios, ai quando eu clico no botão
			que eu defini ali em cima ele troca, de CitacoesExercicios para SobreExercicio-->
		</keep-alive> <!-- Ele mantem o estado do componente vivo, sendo assim quando eu troco
		de citações, para sobre ele volta a onde eu deixei, ele não reinicia o componente.-->

	</div>
</template>

<script>
import CitacoesExercicios from './components/CitacoesExercicios'
import SobreExercicio from './components/SobreExercicio'

export default {
	/* eslint-disable */
	components: { CitacoesExercicios, SobreExercicio },
	data(){
		return {
			componente: 'CitacoesExercicios'
		}
	},
}
</script>

<style>
	#app {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100vh;
		font-size: 1.6rem;
	}

	button {
        outline: none;
        padding: 5px 15px 10px;
        margin: 10px 5px;
        border-radius: 3px;
        font-size: 2rem;
        font-weight: 300;
        color: #FFF;
        background-color: rgba(0, 0, 0, .5);
    }
</style>