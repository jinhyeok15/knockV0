<script>
	import Router, {location} from 'svelte-spa-router';
	import Mydoc from './Mydoc.svelte';
	import Search from './Search.svelte';
	import Package from './Package.svelte';
	import Home from './Home.svelte';

	let routes = {
		"/": Home,
		"/mydoc": Mydoc,
		"/search": Search,
		"/package": Package
	}
</script>

<link href='https://fonts.googleapis.com/css?family=Baloo' rel='stylesheet'>
<main>
	<header>
		<a href="/"><div class="knock"><b>KnocK</b></div></a>
		<div class="nav">
			<div class="bars">
				<div class="mydoc bars_component"><a href="/#/mydoc">내 문서</a></div>
				<div class="search bars_component"><a href="/#/search">검색</a></div>
				<div class="package bars_component"><a href="/#/package">패키지</a></div>
			</div>
		</div>
		<div class="loginbar">
			<div class="login loginbar_component"><a href="/">로그인</a></div>
			<div class="join loginbar_component"><a href="/">회원가입</a></div>
		</div>
	</header>
	<div class="body">
		<Router {routes}/>
	</div>
</main>

<style>
	/* test border */
	/* border: 1px solid; */
	header {
		background-color: white;
		position: absolute;
		height: 120px;
		width: 1440px;
		margin-left: 50%;
		left: -720px;
		top: 0%;
	}
	header div {
		position: absolute;
		top: 30px;
	}
	.body {
		position: absolute;
		width: 1440px;
		height: 900px;
		top: 120px;
		margin-left: 50%;
		left: -720px;
		/* test border */
		border: 1px solid;
	}
	.knock {
		left: 60px;
		width: 160px;
		height: 60px;
		text-align: center;
	}
	.knock b {
		color: #A5D29E;
		font-family: 'Baloo';
		font-size: 40px;
	}

	.nav {
		left: 300px;
		width: 700px;
		height: 60px;
	}
	.bars {
		position: absolute;
		top: 5px;
		left: 100px;
		width: 500px;
		height: 50px;
	}
	.bars_component {
		position: relative;
		top: 0%;
		left: 0%;
		width: 100px;
		height: 50px;
		text-align: center;
		display:table-cell;
		vertical-align:middle; 
	}
	.bars_component a {
		font-size: 17px;
		font-weight: bold;
		color: black;
	}
	.mydoc {left: -1px;}.search {left: 97.5px;}.package {left: 195px;}

	.loginbar {
		right: 60px;
		width: 300px;
		height: 60px;
		float: left;
	}
	.loginbar_component {
		position: relative;
		left: 60px;
		top: 15px;
		font-size: 17px;
		text-align: center;
		display:table-cell;
		vertical-align:middle;
	}
	.loginbar_component a {
		color: black;
	}
	.login {width: 80px; height: 30px;} .join {left: 100px; width: 80px; height: 30px;}
	@media screen and (max-width:1440px) {
		header{left:0%; margin-left:0%;}
		.body{left:0%; margin-left:0%;}
	}
</style>
