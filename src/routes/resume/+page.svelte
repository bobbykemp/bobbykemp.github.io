<script>
	import BackButton from '$lib/components/BackButton.svelte';
	import ResumePreview from '$lib/components/ResumePreview.svelte';
</script>

<BackButton />

<div class="container">
	<ResumePreview width={1200} />
</div>

<style>
	.container {
		height: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
