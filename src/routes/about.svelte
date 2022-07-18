<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>
<link
	rel="stylesheet"
	href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"
/>
<div class="container" id="contacts" />
<br />
<h1 class="home-discription">CONNECT</h1>
<span class="line" />
<br />
<br />
<div class="contat-icon">
	<a href="https://www.linkedin.com/in/anas-alatasi-a7ba64201/" class="fa fa-linkedin" />
	<a href="https://www.facebook.com/anas.atasi" class="fa fa-facebook" />
	<a href="https://www.instagram.com/anasalatasi//" class="fa fa-instagram" />
	<div class="clear" />
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}

	.fa {
		padding: 10px;
		font-size: 20px;
		width: 36px;

		text-align: center;
		text-decoration: none;
	}

	.fa:hover {
		opacity: 0.7;
	}

	.fa-facebook {
		background: #3b5998;
		color: white;
	}
	.fa-instagram {
		background: #ea4c89;
		color: white;
	}
	.fa-linkedin {
		background: #007bb5;
		color: ghostwhite;
	}
	.contact {
		text-align: center;

		position: relative;
	}
	.contact .clear {
		clear: both;
	}
	.contat-icon {
		display: flex;
		justify-content: center;
	}
	.contact h1 {
		font-size: 40px;
		font-family: montserrat, sans-serif;
		font-weight: bold;
	}
	.contact .line {
		position: absolute;
		height: 5px;
		width: 100px;
		left: 600px;
		background-color: #6195ff;
	}
</style>
