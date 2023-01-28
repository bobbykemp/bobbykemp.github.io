<script>
	import profile from '$lib/images/profile.jpeg';
	import Icon from '@iconify/svelte';
</script>

<div class="page">
	<div class="container">
		<img class="profile" src={profile} alt="profile" />
	</div>
	<div class="container">
		<a href="/workplaces">
			<div class="icon-box">
				<Icon href="/workplaces" width="90" icon="ph:map-trifold-duotone" />
				<div>Places I've Worked</div>
			</div>
		</a>
		<a href="/skills">
			<div class="icon-box">
				<Icon width="90" icon="fluent:design-ideas-20-filled" />
				<div>My Skills</div>
			</div>
		</a>
	</div>
</div>
