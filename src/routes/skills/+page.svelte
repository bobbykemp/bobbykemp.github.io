<script>
	import BackButton from '$lib/components/BackButton.svelte';
</script>

<BackButton />

<div class="card">
	<h3 class="card-title"><b>Languages</b></h3>
	<div class="container">
		<p class="card-content">
			Python, JavaScript, React, jQuery, Google Workbox, Docker, Docker Compose, Java, JUnit, C#,
			Git, PowerShell, PowerBI, PowerBI Report Builder, Microsoft Power Apps, Microsoft Power
			Automate, Batch, Bash, Elasticsearch, Logstash, Django, Django-REST Framework, Celery Task
			Queue, SQL (SQLite, MySQL, PostgreSQL), Ubuntu, Ubuntu Server, CentOS, macOS, Windows, Windows
			Server
		</p>
	</div>
</div>

<style>
	.card {
		/* Add shadows to create the "card" effect */
		box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
		transition: 0.3s;
		border-radius: 20px;
	}
	.card-content {
		word-spacing: 0.5em;
		padding: 20px;
	}
	.card-title {
		padding-top: 20px;
		margin: auto;
		text-align: center;
		justify-content: center;
		align-items: center;
	}
	/* On mouse-over, add a deeper shadow */
	.card:hover {
		box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
	}

	/* Add some padding inside the card container */
	.container {
		padding: 2px;
	}
</style>
