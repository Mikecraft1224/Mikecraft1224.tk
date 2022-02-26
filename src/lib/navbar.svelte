<script lang="ts">
	import Dropdown from './dropdown.svelte';
  import NavbarEntry from './navbar_entry.svelte';
</script>

<svelte:head>
	<script src="https://kit.fontawesome.com/95f41e70e9.js" crossorigin="anonymous"></script>
	<link
		rel="stylesheet"
		href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.15.4/css/fontawesome.min.css"
		integrity="sha384-jLKHWM3JRmfMU0A5x5AkjWkw/EYfGUAGagvnfryNV3F9VqM98XiIH7VBGVoxVSc7"
		crossorigin="anonymous"
	/>
</svelte:head>

<nav
	class="group w-full min-h-16 font-sans flex justify-around hover:bg-mainhb transition duration-300 ease-in-out"
>
	<div />
	<div class="text-lg gap-6 flex place-content-end p-3 py-4">
		<NavbarEntry path="/" name="HOME">
			<i class="fa-solid fa-house absolute" slot="img" />
		</NavbarEntry>

    <Dropdown name="PROJEKTE" id="1">
      <i class="fa-solid fa-folder absolute" slot="img"/>
      <div slot="dropcontent">
        <NavbarEntry path="/ " name="Messenger (coming soon)">
          <i class="fa-solid fa-file absolute" slot="img" />
        </NavbarEntry>
        <NavbarEntry path="/ " name="Coming soon">
          <i class="fa-solid fa-file absolute" slot="img" />
        </NavbarEntry>
      </div>
    </Dropdown>

		<NavbarEntry path="/impressum" name="IMPRESSUM">
			<i class="fa-solid fa-user absolute" slot="img" />
		</NavbarEntry>
	</div>
</nav>