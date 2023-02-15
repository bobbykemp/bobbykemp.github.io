<script>
	import Header from './Header.svelte';
	import './styles.css';
</script>

<Header />

<div class="site">
	<slot />
</div>

<style>
	.site {
		margin-top: 150px;
	}
</style>
