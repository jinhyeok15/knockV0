<script>
	import { links } from 'svelte-routing';
	// components
    // exports
    export let navLoc;
</script>
<header>
	<a href="/"><div class="knock"><b>KnocK</b></div></a>
	<div class="nav">
		<div class="bars" use:links>
			<div class="bars_component" id="mydoc-bar">
                <a href="/mydoc" class="{navLoc === 'mydoc' ? 'nav-link-clicked' : 'nav-link'}">내 문서</a>
            </div>
			<div class="bars_component" id="search-bar">
                <a href="/search" class="{navLoc === 'search' ? 'nav-link-clicked' : 'nav-link'}">검색</a>
            </div>
			<div class="bars_component" id="package-bar">
                <a href="/packages" class="{navLoc === 'package' ? 'nav-link-clicked' : 'nav-link'}">패키지</a>
            </div>
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
    .nav-link-clicked:link {
        text-decoration: underline;
    }
	#mydoc-bar {left: -1px;}#search-bar {left: 97.5px;}#package-bar {left: 195px;}
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
