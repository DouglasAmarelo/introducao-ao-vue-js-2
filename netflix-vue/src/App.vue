<template>
	<div class="contain">
		<categoria titulo="Ação"></categoria>
		<categoria titulo="Suspense"></categoria>
	</div>
</template>

<script>
	import Categoria from './components/Categoria.vue'

	export default {
		name: 'app',
		components: {
			Categoria
		},
		categorias:[
		{
			"id":1,
			"titulo":"Terror",
			"filmes":[
				{
				"id":1,
				"titulo":"It: A Coisa",
				"imagem":"http://br.web.img2.acsta.net/pictures/17/03/29/07/56/333222.jpg"
				},
				{
				"id":2,"titulo":"It: A Coisa","imagem":"http://br.web.img2.acsta.net/pictures/17/03/29/07/56/333222.jpg"
				},
				{
				"id":3,"titulo":"It: A Coisa","imagem":"http://br.web.img2.acsta.net/pictures/17/03/29/07/56/333222.jpg"
				},
				{
				"id":4,"titulo":"It: A Coisa","imagem":"http://br.web.img2.acsta.net/pictures/17/03/29/07/56/333222.jpg"
				},
				{
				"id":5,"titulo":"It: A Coisa","imagem":"http://br.web.img2.acsta.net/pictures/17/03/29/07/56/333222.jpg"
				},
				{
				"id":6,"titulo":"It: A Coisa","imagem":"http://br.web.img2.acsta.net/pictures/17/03/29/07/56/333222.jpg"
				},
				{
				"id":7,"titulo":"It: A Coisa","imagem":"http://br.web.img2.acsta.net/pictures/17/03/29/07/56/333222.jpg"
				},
				{
				"id":8,"titulo":"It: A Coisa","imagem":"http://br.web.img2.acsta.net/pictures/17/03/29/07/56/333222.jpg"
				}
			]
			}
	  ],
		data () {
			return {
				nomeProjeto: 'Netflix com Vue',
				intervalo: null
			}
		}
	}
</script>

<style lang="scss">
	@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.css");

body,
	html {
	padding: 0 10px;
	margin: 0;
	background: #0e0f11;
	color: #ecf0f1;
	font-family: 'Open Sans', sans-serif;
	min-height: 100vh;
	display: -webkit-box;
	display: -ms-flexbox;
	display: flex;
	-webkit-box-orient: horizontal;
	-webkit-box-direction: normal;
		-ms-flex-direction: row;
			flex-direction: row;
	-webkit-box-align: center;
		-ms-flex-align: center;
			align-items: center;
	width: 100%;
	}
	* {
	box-sizing: border-box;
	}

	h1,
	p {
	text-align: center;
	}
	p {
	width: 100%;
	max-width: 500px;
	margin: auto;
	}
	a:link,
	a:hover,
	a:active,
	a:visited {
	-webkit-transition: color 150ms;
	transition: color 150ms;
	color: #95a5a6;
	text-decoration: none;
	}
	a:hover {
	color: #7f8c8d;
	text-decoration: underline;
	}
	.contain {
	width: 100%;
	}

	.slider {
		height: 214px;
		position: relative;
		margin: 0;
		padding: 0 4%;
		-ms-touch-action: pan-y;
		touch-action: pan-y;
	}

	.slider h3{
	position: absolute;
	top: 22px;
	z-index: 30;
	}

	.slider .handle.handlePrev {
		left: 11px;

	}

	.slider .handle.handleNext {
		right: 11px;

	}

	.slider .handle.active {
		cursor: pointer;
	}

	.slider .handle {
		background: rgba(20, 20, 20, 0.26);
		position: absolute;
		top: 0;
		height: 251px;
		bottom: 0;
		z-index: 20;
		width: 7%;
		text-align: center;
		-webkit-box-pack: center;
		-webkit-justify-content: center;
		-moz-box-pack: center;
		-ms-flex-pack: center;
		justify-content: center;
		display: -webkit-box;
		display: -webkit-flex;
		display: -moz-box;
		display: -ms-flexbox;
		display: flex;
		color: #fff;
	}

	.fa{
	font-size: 46px;
	margin-top: 120px;
	}

	.row {
	overflow: hidden;
	}
	.row__inner {
	-webkit-transition: 450ms -webkit-transform;
	transition: 450ms -webkit-transform;
	transition: 450ms transform;
	transition: 450ms transform, 450ms -webkit-transform;
	font-size: 0;
	white-space: nowrap;
	margin: 70.3125px 0;
	padding-bottom: 10px;
	}


	.gui-card {
	position: relative;
	display: inline-block;
	width: 250px;
	height: 140.625px;
	margin-right: 10px;
	font-size: 20px;
	cursor: pointer;
	-webkit-transition: 450ms all;
	transition: 450ms all;
	-webkit-transform-origin: center left;
			transform-origin: center left;
	}
	.gui-card__img {
	width: 250px;
	height: 140.625px;
	-o-object-fit: cover;
		object-fit: cover;
	}
	.gui-card__details {
	position: absolute;
	bottom: 0;
	left: 0;
	right: 0;
	top: 0;
	font-size: 10px;
	opacity: 0;
	background: -webkit-linear-gradient(bottom, rgba(0,0,0,0.9) 0%, rgba(0,0,0,0) 100%);
	background: linear-gradient(to top, rgba(0,0,0,0.9) 0%, rgba(0,0,0,0) 100%);
	-webkit-transition: 450ms opacity;
	transition: 450ms opacity;
	}
	.gui-card__details:after,
	.gui-card__details:before {
	content: '';
	position: absolute;
	top: 50%;
	left: 50%;
	display: #000;
	}
	.gui-card__details:after {
	margin-top: -25px;
	margin-left: -25px;
	width: 50px;
	height: 50px;
	border: 3px solid #ecf0f1;
	line-height: 50px;
	text-align: center;
	border-radius: 100%;
	background: rgba(0,0,0,0.5);
	z-index: 1;
	}
	.gui-card__details:before {
	content: '▶';
	left: 0;
	width: 100%;
	font-size: 30px;
	margin-left: 7px;
	margin-top: -13px;
	text-align: center;
	z-index: 2;
	}
	.gui-card:hover .gui-card__details {
	opacity: 1;
	}
	.gui-card__title {
	position: absolute;
	bottom: 0;
	padding: 10px;
	}
	.row__inner:hover {
	-webkit-transform: translate3d(-62.5px, 0, 0);
			transform: translate3d(-62.5px, 0, 0);
	}
	.row__inner:hover .gui-card {
	opacity: 0.3;
	}
	.row__inner:hover .gui-card:hover {
	-webkit-transform: scale(1.5);
			transform: scale(1.5);
	opacity: 1;
	}
	.gui-card:hover ~ .gui-card {
	-webkit-transform: translate3d(125px, 0, 0);
			transform: translate3d(125px, 0, 0);
	}
</style>
