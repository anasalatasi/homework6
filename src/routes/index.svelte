<script context="module">
	export const prerender = true;
</script>

<script>
	import Counter from '$lib/Counter.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<div class="home">
		<div class="over-lay">
			<div class="home-content">
				<h1 class="title">Hello World</h1>
				<p class="home-discription">I'm Anas a Front-End web Developer</p>
			</div>
		</div>
	</div>
</section>

<style>
	/* Home Header*/
	.home {
		height: 100vh;
		background-size: cover;
		background-image: url('https://images.app.goo.gl/gyfTm4oQoZRLPAep7');

		position: relative;
		color: red;
	}
	.over-lay {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		background-color: rgba(0, 0, 0, 0.7);
	}
	.home-content {
		position: absolute;
		top: 50%;
		width: 65%;
		left: 50%;
		transform: translate(-50%, -50%);
		text-align: center;
	}
	.home .title {
		color: ghostwhite;
		font-size: 45px;
		text-transform: uppercase;
		font-family: montserrat, sans-serif;
	}
	button {
		font-family: inherit;
	}

	.home-discription {
		margin: 20px 0px;
		color: ghostwhite;
		letter-spacing: 2px;
		line-height: 1.5px;
	}
</style>
