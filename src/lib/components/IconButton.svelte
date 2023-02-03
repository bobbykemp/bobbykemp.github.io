<!-- Wraps IconCard component with a clickable link -->
<script>
	import IconCard from './IconCard.svelte';
	export let width = '90';
	export let iconClass = '';
	export let buttonText = '';
	export let href = '/';
	export let flexDirection = 'column';
	export let iconColor = '#000000';
	export let textColor = '#000000';
	export let backgroundColor = '#1C516C';
	export let minWidth = '150px';
</script>

<a {href} class="icon-link">
	<IconCard
		{minWidth}
		{flexDirection}
		{width}
		{iconClass}
		{buttonText}
		{iconColor}
		{textColor}
		{backgroundColor}
	/>
</a>

<style>
	.icon-link {
		padding: 15px;
	}
</style>
