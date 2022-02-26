<script lang="ts">
	import '../app.css';
  import Footer from '$lib/footer.svelte';
	import Navbar from '$lib/navbar.svelte';
</script>

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