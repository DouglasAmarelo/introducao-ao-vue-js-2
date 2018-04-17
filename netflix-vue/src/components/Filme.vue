<template>
	<div class="gui-card">
		<div class="gui-card__media">
			<img class="gui-card__img" v-bind:src="imagem" alt="" />
		</div>
		<div class="gui-card__details">
			<div class="gui-card__title">{{ titulo }}</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'Filme',
		props: ['titulo', 'imagem']
	}
</script>
