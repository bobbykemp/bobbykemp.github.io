<script>
	import profile from '$lib/images/profile.jpeg';
	import IconButton from '$lib/components/IconButton.svelte';
</script>

<div class="page">
	<div class="container">
		<img class="profile" src={profile} alt="profile" />
	</div>
	<div class="container">
		<IconButton
			href={'/workplaces'}
			width="90"
			iconClass="ph:map-trifold-duotone"
			buttonText="Places I've Worked"
		/>
		<IconButton
			href={'/skills'}
			width="90"
			iconClass="fluent:design-ideas-20-filled"
			buttonText="My Skills"
		/>
	</div>
</div>

<style>
	.profile {
		border: 10px solid #1c516c;
		border-radius: 50%;
		width: 20em;
		height: 20em;
	}
</style>
