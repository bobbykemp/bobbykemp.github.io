<script>
	import Icon from '@iconify/svelte';
	export let href = '/';
	export let width = '90';
	export let iconClass = '';
	export let buttonText = '';
</script>

<a {href} class="icon-link">
	<div class="icon-box">
		<Icon style="color: #F5F0DD" {width} icon={iconClass} />
		<div style="color: #F5F0DD">{buttonText}</div>
	</div>
</a>

<style>
	.icon-link {
		padding: 15px;
	}
	.icon-box {
		background-color: #1c516c;
		box-shadow: 10px 5px 5px -2px #888888;
		border-radius: 10px;
		display: flex;
		height: auto;
		flex-direction: column;
		align-items: center;
		width: 100px;
		min-width: 150px;
		text-align: center;
		padding: 0.5em;
	}
</style>
