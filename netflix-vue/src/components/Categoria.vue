<template>
	<div class="slider">
		<h3>{{ titulo }}</h3>

		<!-- Arrow Left -->
		<span v-on:mouseover="scrollEsquerda()" v-on:mouseout="clearScroll()" class="handle handlePrev active">
			<i class="fa fa-caret-left" aria-hidden="true"></i>
		</span>
		<!-- /Arrow Left -->

		<div ref="scroller" class="row">
			<div class="row__inner">

				<filme titulo="Opa" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></filme>
				<filme titulo="Opa" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></filme>
				<filme titulo="Opa" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></filme>
				<filme titulo="Opa" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></filme>
				<filme titulo="Opa" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></filme>
				<filme titulo="Opa" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></filme>
				<filme titulo="Opa" imagem="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700"></filme>

			</div>
		</div>

		<!-- Arrow Right -->
		<span v-on:mouseover="scrollDireita()" v-on:mouseout="clearScroll()"  class="handle handleNext active">
			<i class="fa fa-caret-right" aria-hidden="true"></i>
		</span>
		<!-- /Arrow Right -->
	</div>
</template>

<script>
	import Filme from './Filme.vue';

	export default {
		name: 'Categoria',
		props: ['titulo'],
		components: {
			Filme
		},
		methods: {
			scrollDireita() {
				this.intervalo = setInterval(() => {
					this.$refs.scroller.scrollLeft += 1
				}, 5);
			},
			scrollEsquerda() {
				this.intervalo = setInterval(() => {
					this.$refs.scroller.scrollLeft -= 1
				}, 5);
			},
			clearScroll() {
				clearInterval( this.intervalo );
			}
		}
	}
</script>
