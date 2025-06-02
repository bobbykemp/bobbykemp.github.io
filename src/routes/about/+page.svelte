<script>
	import BackButton from '$lib/components/BackButton.svelte';
</script>

<div class="page">
	<BackButton />
	<div class="about">
		<p>Hi, I'm Bobby Kemp.</p>
		<p>
			I'm a full-stack software engineer with a focus on building scalable, real-time systems and
			robust backend services using Spring Boot and Django REST. I've led the development of
			full-stack, containerized applications—often deployed with Docker and managed through CI/CD
			pipelines using Jenkins and Git.
		</p>
		<p>
			My work spans enterprise modernization, point-of-sale system integrations, and
			performance-critical pipelines. I've built and maintained RESTful APIs, implemented secure
			authentication flows with Keycloak (OAuth2), and integrated with legacy systems like IBM i
			(AS/400) via JT400. My frontend experience includes modern web technologies like React and
			Svelte, often deployed as Progressive Web Apps.
		</p>
		<p>
			Whether I'm replacing an FTP batch job with a performant Spring Batch system or engineering a
			real-time computer vision pipeline with a frontend dashboard, I bring a deep understanding of
			system design, user experience, and cross-functional collaboration. I care about building
			software that not only works, but endures—and I thrive in teams where technical ownership and
			autonomy are valued.
		</p>
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Eczar&display=swap');
	.page {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		padding: 1rem;
		box-sizing: border-box;
	}

	.about {
		text-align: center;
		max-width: 1200px;
		margin: 0 auto;
		padding: 1em;
	}
	p {
		font-family: 'Eczar', serif;
		font-size: 1.3em;
	}
</style>
