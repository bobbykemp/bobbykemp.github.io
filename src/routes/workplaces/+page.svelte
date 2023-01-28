<script>
	import map from '$lib/images/map.png';
	import BackButton from '$lib/components/BackButton.svelte';
	import LocationDot from './LocationDot.svelte';

	let workplaceText = '';

	const workplaceDescriptions = {
		arlington: 'Arlington',
		burlington: 'Burlington',
		davenport: 'Davenport'
	};
</script>

<BackButton />

<div class="page">
	<div class="map">
		<img class="map" src={map} alt="U.S. map" />
		<LocationDot
			top={253}
			left={273}
			onClick={() => (workplaceText = workplaceDescriptions.arlington)}
		/>
		<LocationDot
			top={133}
			left={331}
			onClick={() => (workplaceText = workplaceDescriptions.burlington)}
		/>
		<LocationDot
			top={120}
			left={337}
			onClick={() => (workplaceText = workplaceDescriptions.davenport)}
		/>
	</div>
</div>
{workplaceText}
