<script>
	import resume from '$lib/files/BobbyKempResume.pdf';
	export let width = 300;
	export let height = 600;
</script>

<embed type="application/pdf" src={resume} {width} {height} />
