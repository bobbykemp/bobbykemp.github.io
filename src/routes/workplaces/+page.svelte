<script>
	import iowaMap from '$lib/images/iowa.png';
	import texasMap from '$lib/images/texas.png';
	import BackButton from '$lib/components/BackButton.svelte';
	import LocationDot from '$lib/components/LocationDot.svelte';
	import Tooltip from '$lib/components/Tooltip.svelte';
	import Modal from '$lib/components/Modal.svelte';

	let workplaceText = '';
	let modalVisible = false;

	const workplaces = [
		{
			shortName: 'Arlington',
			longName: 'Arlington, Texas',
			position: {
				top: 334,
				left: 217
			},
			description: `<h3>College in Arlington</h3>
			<h5>August 2016 - May 2020</h5>
			<p>
				I moved to Arlington, Texas after graduating salutatorian from Burlington 
				Highschool. While living in Arlington, I pursused a degree in Computer 
				Science with a minor in Business Information Systems at the University 
				of Texas at Arlington (Go Mavs!).
			</p>
			<p>
				In 2020 I graduated Magna Cum Laude with an Honors Bachelor 
				of Science in Computer Science and a minor in Business Information Systems.
			</p>
			<p>
				During my four year degree at UTA, I participated in various
				honors societies on campus, including:
			<ul>
				<li>Tau Beta Pi Engineering Honors Society</li>
				<li>Upsilon Pi Epsilon Computing and Information Honors Society</li>
				<li>Phi Kappa Phi Honors Society</li>
				<li>Golden Key Honors Society</li>
			</ul>
			<p>
				These societies provided great opportunities to meet like-minded peers and 
				participate in charity events all over the Dallas Fort-Worth area.
			</p>
			<p>
				While at UTA I also served as Vice President of the Game Developers Club
				Junior and Senior year. GDC was the perfect club for aspiring
				game developers. We held weekly meetings discussing different engines, new 
				technologies, and design principles for building games effectively. We also 
				held the occasional game jam to put our skills to the test!
			</p>
			`
		},
		{
			shortName: 'Ft. Worth',
			longName: 'Fort Worth, Texas',
			position: {
				top: 319,
				left: 233
			},
			description: `
			<h3>Working at Herzog Technologies (HTIX)</h3>
			<h5>June 2019 – June 2020; June 2020 - February 2022</h5>
			<p>
				I started out as an intern during the summer of my junior year of college 
				at Herzog Technologies.
			</p>
			<p>
				As an intern I got my first exposure to creating full-stack web applications
				using Django, DjangoREST, and React JS. After first working with the senior engineer to write unit tests
				for the DjangoREST backend, I was eventually tasked with designing, developing, and maintaining
				a full-stack, fully offline-capable web application that would allow technicians to digitally fill out
				inspection reports for critical network infrastructure while in the field.
			</p> 
			<p>
				During my time at Herzog I also got to work with Elasticsearch, Logstash, 
				and Kibana (the ELK stack). Being a leader in PTC hosting, one of HTIX's main 
				daily operations was analyzing logs pulled off of locomotives operating all over the country.
				This meant ingesting millions of logs every day, and having several healthy Elasticsearch 
				clusters helped immensely in reducing the time the operations department had to 
				take to analyze these logs daily.
			</p>
			`
		},
		{
			shortName: 'Burlington',
			longName: 'Burlington, Iowa',
			position: {
				top: 164,
				left: 262
			},
			description: `<h3>Internship at Federal Mogul (My First Job)</h3>
			<h5>May 2017 – August 2017; May 2018 – August 2018</h5>
			<p>
				I grew up in Burlington, Iowa. My first job was at the Federal Mogul (Champion Spark Plugs) plant in town.
				I was a safety and maintenance department intern for two summers, during which I helped create somewhere around 
				200 unique Lock Out Tag Out forms for the plant's various machines.
			</p>
			<p>
				During my second summer, the maintenance department brought me in to help them automate some of 
				the manual paperwork that they had to do on a daily basis. My work with them helped them save around 5 
				hours per week of manual paperwork.
			</p>`
		},
		{
			shortName: 'Davenport',
			longName: 'Davenport, Iowa',
			position: {
				top: 118,
				left: 280
			},
			description: `<h3>Working at Iowa 80 Group</h3>
			<h5>March 2022 - Present</h5>
			<p>
				After working at Herzog for almost three years and living in Texas for about six, I decided
				to move back home to Iowa.
			</p>
			<p>
				I joined up with Iowa 80 Group in Walcott, Iowa as a Software Engineer. While working
				on the campus of the World's Largest Truckstop, I developed a full-stack web application to help
				the Iowa80.com shipping and receiving department catalog photos of damaged inventory.
				I developed a second full-stack web application to replace a legacy Access inventory management application.
				I also assisted in the development and deployment of the new point-of-sale application for the Truckomat truck wash,
				and assisted in the modernization of various legacy green screen applications and reports to modern web applications.
			</p>
			`
		}
	];
</script>

<BackButton />

{#if modalVisible}
	<Modal on:close={() => (modalVisible = false)}>{@html workplaceText}</Modal>
{/if}

<div class="page">
	<p><i>Click the pins on the map to explore where I've been, and what I've done there!</i></p>
	<div class="map">
		<img src={iowaMap} alt="Iowa map" />
		<img src={texasMap} alt="Texas map" />
		{#each workplaces as workplace}
			<Tooltip
				title={workplace.longName}
				top={workplace.position.top + 20}
				left={workplace.position.left + 20}
			>
				<LocationDot
					top={workplace.position.top}
					left={workplace.position.left}
					onClick={() => {
						modalVisible = true;
						workplaceText = workplace.description;
					}}
				/>
			</Tooltip>
		{/each}
	</div>
</div>

<style>
	h4 {
		padding: 5px;
	}
	.map {
		position: relative;
		display: inline-block;
	}

	.map img {
		display: block;
		max-width: 325px;
		height: auto;
	}
</style>
