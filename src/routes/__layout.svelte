<script lang="ts">
  import { onMount } from 'svelte/internal';
	import '../app.css';
  import Footer from '$lib/footer.svelte';
	import Navbar from '$lib/navbar.svelte';

  onMount(() => {
    document.getElementById("copy").addEventListener("copy", function(e) {
      e.clipboardData.setData("text/plain", "Hallo Verwi c:");
      e.preventDefault();
    })
  })
</script>

<svelte:head>
  <link rel='icon' type='image/vnd.microsoft.icon' href='/Icon.ico'>
</svelte:head>

<div id="copy">
  <Navbar />

  <slot />

  <Footer />
</div>

<style>
	:global(body) {
		--main-background: #111;

		background-image: url('/code_wallpaper.svg');
		background-repeat: no-repeat;
		background-attachment: fixed;
		background-position: center;
		background-size: auto;

		background-color: var(--main-background);
    color: #ffffff;
	}
</style>