<script>
	let linkStatus = { clicked: false };

	function toggle() {
		user.loggedIn = !user.loggedIn;
	}
    export let path;
    export let navName;
</script>

{#if !linkStatus.clicked}
	<a href={path} class="nav-link" id="unclicked-nav" on:click={toggle}>
		{navName}
    </a>
{:else}
	<a href={path} class="nav-link" id="clicked-nav" on:click={toggle}>
		{navName}
    </a>
{/if}


<style>
    .nav-link {
        font-size: 17px;
		font-weight: bold;
		color: black;
    }
    #clicked-nav {
        text-decoration: underline;
    }
</style>
