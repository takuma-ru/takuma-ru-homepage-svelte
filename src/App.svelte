<script lang="ts">
	import { Router, Link, Route } from 'svelte-routing';
	// pages
	import Top from './pages/top.svelte'
	import About from './pages/about.svelte'

	//componets
	import Frame from './components/frame.svelte'
</script>

<Router>
	<Frame></Frame>
	<Link to="">home</Link>
	<Link to="about">about</Link>
	<main>
		<Route path="" component={Top} />
		<Route path="about" component={About} />
	</main>
</Router>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
</style>