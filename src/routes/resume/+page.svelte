<script>
	import BackButton from '$lib/components/BackButton.svelte';
	import ResumePreview from '$lib/components/ResumePreview.svelte';
</script>

<BackButton />

<div class="container">
	<ResumePreview width={1200} height={550} />
</div>

<style>
	.container {
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
