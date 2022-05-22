<script>
	import { links } from 'svelte-routing';
	// components
  // exports
  export let navLoc;
</script>
<header>
	<a href="/"><div class="knock"><b>KnocK</b></div></a>
	<div class="navbar" use:links>
		<div class="nav-components" id="mydoc-bar">
			<a href="/mydoc" class="{navLoc === 'mydoc' ? 'nav-link-clicked' : 'nav-link'}">
				<div class="nav-text-component">내 문서</div>
			</a>
		</div>
		<div class="nav-components" id="search-bar">
			<a href="/search" class="{navLoc === 'search' ? 'nav-link-clicked' : 'nav-link'}">
				<div class="nav-text-component">검색</div>
			</a>
		</div>
		<div class="nav-components" id="package-bar">
			<a href="/packages" class="{navLoc === 'package' ? 'nav-link-clicked' : 'nav-link'}">
				<div class="nav-text-component">패키지</div>
			</a>
		</div>
	</div>
	<div class="loginbar">
		<div class="login loginbar_component"><a href="/">로그인</a></div>
		<div class="join loginbar_component"><a href="/">회원가입</a></div>
	</div>
</header>

<style>
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
    .navbar {
		left: 300px;
		width: 700px;
		height: 60px;
	}
	.nav-components {
		position: absolute;
		top: 5px;
		left: 100px;
		width: 100px;
		height: 50px;
		text-align: center;
	}
    .nav-components a {
        font-size: 17px;
		font-weight: bold;
		color: black;
    }
	.nav-text-component {
		position: relative;
		top: 15px;
		width: 100%;
		height: 20px;
		display: table-cell;
		vertical-align:middle;
	}
    .nav-link-clicked:link {
        text-decoration: underline;
    }
	#mydoc-bar {left: 100px;} #search-bar {left: 300px;} #package-bar {left: 500px;}
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
</style>
