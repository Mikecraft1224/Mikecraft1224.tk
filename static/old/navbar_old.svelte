<script lang="ts">
	let act = false;

	function enter() {
		act = true;
	}

	function leave() {
		act = false;
	}
</script>

<nav class="nav-bar">
	<a class="nav-link active" href="#home">Home</a>

	<div class="dropdown" id="project" class:act on:click={enter} on:mouseleave={leave}>
		<a class="nav-link dropbtn hover:outline hover:outline-1" href="#project">Projekte</a>
		<div class="dropcontent outline outline-1">
			<a class="nav-link" href="/">Projekt1</a>
			<a class="nav-link" href="/">Projekt2</a>
		</div>
	</div>

	<a class="nav-link" href="./impressum.html">Impressum</a>
</nav>

<style>
	:root {
		--main-header-background: #545d63;
		--main-fonts-color: #1d1b1a;
		--hover-fonts-color: #d6cecc;
		--main-font-family: 'Poppins', sans-serif;
		--main-decor-color: #708787;

		color: #293133;
	}

	/*Nav*/

	.nav-bar {
		margin: 0 auto;
		width: 100%;
		height: 70px;
		display: flex;
		align-items: center;
		justify-content: space-around;
		background: transparent;
		position: fixed;
		top: 0;
		transition: 0.3s;
		z-index: 5;
	}

	.nav-bar:hover {
		background: var(--main-header-background);
	}

	.nav-bar {
		list-style: none;
		position: relative;
		display: inline-flex;
	}

	a.nav-link {
		margin: 2px;
		padding: 5px 10px;
		text-decoration: none;
		color: var(--main-fonts-color);
		font-family: var(--main-font-family);
		text-transform: uppercase;
	}

	.active {
		background: var(--main-decor-color);
	}

	.nav-link:hover {
		color: var(--hover-fonts-color);
		background: var(--main-decor-color);
	}

	/*Dropdown */

	.dropbtn {
		padding: 16px;
		border: none;
	}

	.dropdown {
		position: relative;
		display: inline-block;
	}

	.dropcontent {
		display: none;
		position: absolute;
		background-color: var(--main-header-background);
		min-width: 150px;
		z-index: 1;
	}

	.dropcontent a {
		padding: 5px 10px;
		display: block;
	}

	.dropcontent a:hover {
		color: var(--hover-fonts-color);
		background: var(--main-decor-color);
	}

	.dropdown a:hover a.dropbtn {
		background-color: var(--main-decor-color);
	}

	.act .dropcontent {
		display: block;
	}
</style>
