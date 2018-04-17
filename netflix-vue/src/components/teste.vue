<template>
	<h1>{{ titulo }}</h1>
</template>

<script>
	export default {
		name: 'teste',
		props: ['titulo']
	}
</script>

<style lang="sass">
	h1 { color: red; }
</style>
