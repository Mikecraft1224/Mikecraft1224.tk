<script lang="ts">
	import '../app.css';
  import Footer from '$lib/footer.svelte';
	import Navbar from '$lib/navbar.svelte';
</script>

<svelte:head>
  <link rel='icon' type='image/vnd.microsoft.icon' href='/Icon.ico'>
</svelte:head>

<Navbar />

<slot />

<Footer />

<style>
	:global(body) {
		--main-background: #aaaaaa;

		background-image: url('/Background_trans.svg');
		background-repeat: no-repeat;
		background-attachment: fixed;
		background-position: center;
		background-size: cover;

		background-color: var(--main-background);
    color: #293133;
	}
</style>