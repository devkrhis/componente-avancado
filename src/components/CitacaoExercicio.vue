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
    // Created e destroyed, eles criam e destroiem o componente, porém só aparece se não estiver com keep-alive.
	created(){
		console.log('created')
	},
	destroyed(){
		console.log('destroyed')
	},
	// Activated e deactivated, eles ativam e desativam o componente, porém só aparece se estiver com o keep-alive.
	activated(){
		console.log('activated')
	},
	deactivated(){
		console.log('deactivated')

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
