<script>
	import {Router, Route} from 'svelte-routing';
	import Mydoc from './mydoc/Mydoc.svelte';
	import Search from './search/Search.svelte';
	import Package from './package/Package.svelte';
	import Home from './home/Home.svelte';
	// components

	export let url = "";
</script>

<link href='https://fonts.googleapis.com/css?family=Baloo' rel='stylesheet'>

<Router url="{url}">
	<main>
		<Route path="/" component="{Home}"/>
		<Route path="mydoc" component="{Mydoc}"/>
		<Route path="search" component="{Search}"/>
		<Route path="packages" component="{Package}"/>
	</main>	
</Router>

<style>
	/* test border */
	/* border: 1px solid; */
	main {
		position: absolute;
		width: 1440px;
		margin-left: 50%;
		left: -720px;
	}
	
	@media screen and (max-width:1440px) {
		main {margin-left: 0%; left: 0%;}
	}
</style>
