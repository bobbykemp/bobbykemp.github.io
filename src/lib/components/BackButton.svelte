<script>
	import Icon from '@iconify/svelte';
	export let href = '/';
</script>

<a class="back-button" {href}>
	<Icon class="back-icon" icon="mdi:arrow-back-circle" width="30" />
</a>

<style>
	.back-button {
		position: fixed;
		z-index: 101;
		top: 10px;
		left: 10px;
	}
</style>
