<script lang="ts">
	import image from "images/successkid.jpg";

	import { onMount } from "svelte";
	onMount(() => {
		console.log("Functions are coming...");

		fetch("/.netlify/functions/hello")
			.then((response) => response.json())
			.then((json) => console.log(json));
	});
</script>

<style>
</style>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>

<h1 class="text-2xl">Great success!</h1>

<p>See the function running in the console</p>

<img src={image} alt="" />

<p>
	<strong>Try editing this file (src/routes/index.svelte) to test live
		reloading.</strong>
</p>
