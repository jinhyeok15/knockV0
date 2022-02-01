<script>
	let linkStatus = { clicked: false };

	function toggle() {
		linkStatus.clicked = !linkStatus.clicked;
	}
    export let path;
    export let navName;
    export let navId;
</script>

{#if !linkStatus.clicked}
	<a href={path} class="nav-link" id={navId} on:click={toggle}>
		{navName}
    </a>
{:else}
	<a href={path} class="nav-link" id={navId} on:click={toggle}>
		{navName}
    </a>
{/if}


<style>
    .nav-link {
        font-size: 17px;
		font-weight: bold;
		color: black;
    }
</style>
