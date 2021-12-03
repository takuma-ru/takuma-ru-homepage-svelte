<script lang="ts">
	import Router from 'svelte-spa-router'
	import { routes } from './router'
	// pages
	import Top from './pages/top.svelte'
	import About from './pages/about.svelte'

	//componets
	import Frame from './components/frame.svelte'

	export let url = "";
</script>

<Frame></Frame>
<main>
	<Router {routes} />
</main>

<style>
main {
	text-align: center;
	width: calc(100vw - 96px);
	margin-left: 48px;
	padding-top: 48px;
	min-height: calc(100vh - 96px);
}
</style>