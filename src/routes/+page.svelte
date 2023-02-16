<script>
	import profile from '$lib/images/profile.jpeg';
	import IconButton from '$lib/components/IconButton.svelte';
</script>

<div class="page">
	<div class="container">
		<img class="profile" src={profile} alt="profile" />
	</div>
	<div class="container" style="justify-content: center">
		<IconButton
			minWidth="90px"
			href={'https://www.linkedin.com/in/bobby-kemp'}
			width="20"
			iconClass="mdi:linkedin"
			buttonText="LinkedIn"
			iconColor="#F5F0DD"
			textColor="#F5F0DD"
			backgroundColor="#953638"
			flexDirection="row"
		/>
		<IconButton
			minWidth="90px"
			href={'https://github.com/bobbykemp'}
			width="20"
			iconClass="mdi:github"
			buttonText="GitHub"
			iconColor="#F5F0DD"
			textColor="#F5F0DD"
			backgroundColor="#953638"
			flexDirection="row"
		/>
		<IconButton
			minWidth="90px"
			href={'/resume'}
			width="20"
			iconClass="mdi:resume"
			buttonText="Resume"
			iconColor="#F5F0DD"
			textColor="#F5F0DD"
			backgroundColor="#953638"
			flexDirection="row"
		/>
	</div>
	<div class="container" style="max-width: 750px;">
		<IconButton
			href={'/about'}
			width="70"
			iconClass="mdi:about-circle-outline"
			buttonText="About me"
			iconColor="#F5F0DD"
			textColor="#F5F0DD"
		/>
		<IconButton
			href={'/workplaces'}
			width="70"
			iconClass="ph:map-trifold-duotone"
			buttonText="Places I've Worked"
			iconColor="#F5F0DD"
			textColor="#F5F0DD"
		/>
		<IconButton
			href={'/skills'}
			width="70"
			iconClass="fluent:design-ideas-20-filled"
			buttonText="My Skills"
			iconColor="#F5F0DD"
			textColor="#F5F0DD"
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
