<script>
	export let top = 0;
	export let left = 0;
	export let onClick = () => {};
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<svg
	style={`top: ${top}px; left: ${left}px`}
	viewBox="0 0 100 100"
	class="target"
	xmlns="http://www.w3.org/2000/svg"
	on:click={onClick}
>
	<circle cx="50" cy="50" r="50" />
</svg>

<style>
	.target {
		cursor: pointer;
		padding: 4px;
		z-index: 9;
		position: absolute;
		width: 10px;
	}
</style>
