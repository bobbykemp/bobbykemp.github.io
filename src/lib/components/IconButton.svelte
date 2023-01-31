<!-- Wraps IconCard component with a clickable link -->
<script>
	import IconCard from './IconCard.svelte';
	export let width = '90';
	export let iconClass = '';
	export let buttonText = '';
	export let href = '/';
	export let iconColor = '#000000';
	export let textColor = '#000000';
</script>

<a {href} class="icon-link">
	<IconCard {width} {iconClass} {buttonText} {iconColor} {textColor} />
</a>

<style>
	.icon-link {
		padding: 15px;
	}
</style>
