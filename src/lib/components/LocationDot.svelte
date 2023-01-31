<script>
	import Icon from '@iconify/svelte';
	export let top = 0;
	export let left = 0;
	export let onClick = () => {};
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div style={`top: ${top}px; left: ${left}px`} class="target" on:click={onClick}>
	<Icon style="color: #F5F0DD" icon="material-symbols:push-pin-outline" />
</div>

<style>
	.target {
		cursor: pointer;
		padding: 4px;
		z-index: 9;
		position: absolute;
		width: 15px;
	}
</style>
