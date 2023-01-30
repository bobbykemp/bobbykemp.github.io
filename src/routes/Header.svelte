<header>
	<div class="main">Bobby Kemp</div>
	<div class="secondary-container">
		<div class="typewriter">Software Engineer</div>
	</div>
</header>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Eczar&display=swap');
	header {
		display: flex;
		flex-wrap: wrap;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	div.main {
		font-family: 'Eczar', serif;
		font-size: 2.3em;
	}
	div.secondary-container {
		display: flex;
		justify-content: center;
		padding-bottom: 20px;
	}
	.typewriter {
		overflow: hidden; /* Ensures the content is not revealed until the animation */
		border-right: 0.15em solid orange; /* The typwriter cursor */
		white-space: nowrap; /* Keeps the content on a single line */
		margin: 0 auto; /* Gives that scrolling effect as the typing happens */
		letter-spacing: 0.15em; /* Adjust as needed */
		animation: typing 2s steps(20, end), blink-caret 0.75s step-end infinite;
	}

	/* The typing effect */
	@keyframes typing {
		from {
			width: 0;
		}
		to {
			width: 100%;
		}
	}

	/* The typewriter cursor effect */
	@keyframes blink-caret {
		from,
		to {
			border-color: transparent;
		}
		50% {
			border-color: rgb(128, 128, 128);
		}
	}
</style>
