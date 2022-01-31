<script>
	export let name;
</script>

<div class="header">
	<div class="Knock"></div>
	<div class="Nav"></div>
	<div class="LoginBar"></div>
</div>

<style>
	.header {
		background-color: silver;
		position: absolute;
		height: 120px;
		width: 1440px;
		margin-left: 50%;
		left: -720px;
		top: 0%;
	}
	.header div {
		position: absolute;
		top: 30px;
	}
	.Knock {
		background-color: #A5D29E;
		left: 60px;
		width: 160px;
		height: 60px;
	}
	.Nav {
		background-color: yellow;
		left: 300px;
		width: 700px;
		height: 60px;
	}
	.LoginBar {
		background-color: blue;
		right: 60px;
		width: 300px;
		height: 60px;
	}
</style>