<script>
	export let title = '';
	export let top = 0;
	export let left = 0;
	let isHovered = false;

	function mouseOver() {
		isHovered = true;
	}
	function mouseLeave() {
		isHovered = false;
	}
</script>

<!-- svelte-ignore a11y-mouse-events-have-key-events -->
<span on:mouseover={mouseOver} on:mouseleave={mouseLeave}>
	<slot />
</span>

{#if isHovered}
	<span style="top: {top}px; left: {left}px;" class="tooltip">{title}</span>
{/if}

<style>
	.tooltip {
		z-index: 9;
		border: 1px solid rgb(128, 128, 128);
		box-shadow: 1px 1px 1px #ddd;
		background: rgb(128, 128, 128);
		border-radius: 4px;
		padding: 4px;
		position: absolute;
	}
</style>
