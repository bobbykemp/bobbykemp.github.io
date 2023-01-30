<script>
	import Icon from '@iconify/svelte';
	export let href = '/';
	export let width = '90';
	export let iconClass = '';
	export let buttonText = '';
</script>

<a {href}>
	<div class="icon-box">
		<Icon {width} icon={iconClass} />
		<div>{buttonText}</div>
	</div>
</a>

<style>
	.icon-box {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100px;
		text-align: center;
	}
</style>
