<script>
	import BackButton from '$lib/components/BackButton.svelte';
	import IconCard from '$lib/components/IconCard.svelte';

	const width = '30';
	const flexDirection = 'row';

	const orange = '#FDA649';
	const ivory = '#F5F0DD';

	const skills = {
		languages: [
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:language-javascript',
				buttonText: 'JavaScript'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:language-python',
				buttonText: 'Python'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:language-java',
				buttonText: 'Java'
			}
		],
		frameworks: [
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:react',
				buttonText: 'React'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'file-icons:workbox',
				buttonText: 'Workbox'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'simple-icons:django',
				buttonText: 'Django & Django REST'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'simple-icons:celery',
				buttonText: 'Celery Task Queue'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:jquery',
				buttonText: 'JQuery'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'simple-icons:junit5',
				buttonText: 'JUnit'
			}
		],
		devops: [
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:git',
				buttonText: 'Git'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:docker',
				buttonText: 'Docker'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:powershell',
				buttonText: 'PowerShell'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:bash',
				buttonText: 'Bash'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'vscode-icons:file-type-makefile',
				buttonText: 'GNU make'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'simple-icons:elasticsearch',
				buttonText: 'ElasticSearch'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'simple-icons:elasticsearch',
				buttonText: 'Logstash'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'simple-icons:kibana',
				buttonText: 'Kibana'
			}
		],
		databases: [
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'tabler:brand-mysql',
				buttonText: 'MySQL'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'carbon:ibm-db2-alt',
				buttonText: 'DB2'
			}
		],
		systems: [
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:ubuntu',
				buttonText: 'Ubuntu & Ubuntu Server'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:centos',
				buttonText: 'CentOS'
			},
			{
				iconColor: ivory,
				textColor: ivory,
				iconClass: 'mdi:microsoft-windows',
				buttonText: 'Windows Server'
			}
		]
	};
</script>

<BackButton />

<h3 class="card-title"><b>Languages</b></h3>
<div class="container">
	{#each skills.languages as skill, index}
		<div class="animation-wrapper" style="--animation-order: {index};">
			<IconCard
				{width}
				{flexDirection}
				iconColor={skill.iconColor}
				textColor={skill.textColor}
				iconClass={skill.iconClass}
				buttonText={skill.buttonText}
			/>
		</div>
	{/each}
</div>
<h3 class="card-title"><b>Frameworks</b></h3>
<div class="container">
	{#each skills.frameworks as skill, index}
		<div class="animation-wrapper" style="--animation-order: {skills.languages.length + index};">
			<IconCard
				{width}
				{flexDirection}
				iconColor={skill.iconColor}
				textColor={skill.textColor}
				iconClass={skill.iconClass}
				buttonText={skill.buttonText}
				backgroundColor={orange}
			/>
		</div>
	{/each}
</div>
<h3 class="card-title"><b>Devops</b></h3>
<div class="container">
	{#each skills.devops as skill, index}
		<div
			class="animation-wrapper"
			style="--animation-order: {skills.languages.length + skills.frameworks.length + index};"
		>
			<IconCard
				{width}
				{flexDirection}
				iconColor={skill.iconColor}
				textColor={skill.textColor}
				iconClass={skill.iconClass}
				buttonText={skill.buttonText}
			/>
		</div>
	{/each}
</div>
<h3 class="card-title"><b>Databases</b></h3>
<div class="container">
	{#each skills.databases as skill, index}
		<div
			class="animation-wrapper"
			style="--animation-order: {skills.languages.length +
				skills.frameworks.length +
				skills.devops.length +
				index};"
		>
			<IconCard
				{width}
				{flexDirection}
				iconColor={skill.iconColor}
				textColor={skill.textColor}
				iconClass={skill.iconClass}
				buttonText={skill.buttonText}
				backgroundColor={orange}
			/>
		</div>
	{/each}
</div>
<h3 class="card-title"><b>Systems</b></h3>
<div class="container">
	{#each skills.systems as skill, index}
		<div
			class="animation-wrapper"
			style="--animation-order: {skills.languages.length +
				skills.frameworks.length +
				skills.devops.length +
				skills.databases.length +
				index};"
		>
			<IconCard
				{width}
				{flexDirection}
				iconColor={skill.iconColor}
				textColor={skill.textColor}
				iconClass={skill.iconClass}
				buttonText={skill.buttonText}
			/>
		</div>
	{/each}
</div>

<style>
	.card-title {
		padding-top: 20px;
		margin: auto;
		text-align: center;
		justify-content: center;
		align-items: center;
	}
	.container {
		padding: 2px;
		justify-content: center;
		align-items: left;
	}
	.animation-wrapper {
		animation-name: animateIn;
		animation-duration: 350ms;
		animation-delay: calc(var(--animation-order) * 100ms);
		animation-fill-mode: both;
		animation-timing-function: ease-in-out;
	}
	@keyframes animateIn {
		0% {
			opacity: 0;
			transform: scale(0.6) translateY(-8px);
		}

		100% {
			opacity: 1;
		}
	}
</style>
