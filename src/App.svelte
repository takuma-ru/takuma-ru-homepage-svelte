<script lang="ts">
	import Router from 'svelte-spa-router'
	import { routes } from './router'

	//componets
	import Frame from './components/frame.svelte'

	export let url = "";
</script>

<main>
	<Router {routes} />
</main>
<Frame></Frame>
<div class="deco_background" />

<style>
:global(body) {
	background-color: #FEFEFE;
}

main {
	position: relative;
	width: calc(100vw - 96px);
	min-height: calc(100vh - 96px);
	margin-left: 48px;
	padding-top: 48px;
	text-align: center;
}

.deco_background {
	position: fixed;
	width: 70vmin;
	height: 70vmin;
	left: 0%;
	top: -25%;

	border: 3px solid #0084AD42;
	box-sizing: border-box;
	transform: rotate(30deg);

	animation: anim_back 180s linear 0s infinite normal none;
}

@keyframes anim_back {
	0% {
		transform: rotate(30deg);
	}
	100% {
		transform: rotate(390deg);
	}
}
</style>