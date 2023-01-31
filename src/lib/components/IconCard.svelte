<script>
	import Icon from '@iconify/svelte';
	export let width = '90';
	export let iconClass = '';
	export let buttonText = '';
	export let flexDirection = 'column';
	export let iconColor = '#000000';
	export let textColor = '#000000';
	export let padding = '10px';
	export let backgroundColor = '#1C516C';
</script>

<div
	class="icon-box"
	style="flex-direction: {flexDirection}; background-color: {backgroundColor}; padding: {padding}"
>
	<Icon style="color: {iconColor}" {width} icon={iconClass} />
	{#if buttonText.length > 0}
		<div style="color: {textColor}">{buttonText}</div>
	{/if}
</div>

<style>
	.icon-box {
		align-items: center;
		justify-content: space-evenly;
		box-shadow: 10px 5px 5px -2px #888888;
		border-radius: 10px;
		display: flex;
		height: auto;
		width: 100px;
		min-width: 150px;
		text-align: center;
		padding: 0.5em;
		margin: 5px;
	}
</style>
