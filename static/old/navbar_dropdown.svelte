<script lang="ts">
	import { page } from '$app/stores';
	export let path: string, name;

  let open = false;
</script>

<div on:mouseenter={() => {open = !open}} on:mouseleave={() => {open = !open}}>
	<a href={path}
		class="{$page.url.pathname == path
			? 'actice bg-mainhb text-hoverhf group-hover:bg-hoverhb group-hover:text-mainhf'
			: '!active hover:bg-hoverhb hover:text-hoverhf'} px-4 py-1 rounded-md flex items-center transition duration-300 ease-out">
    {#if open}
	  	<slot name="img2" />
    {:else}
      <slot name="img1" />
    {/if}
    <div class="pl-4">&#8192;| {name}</div>
  </a>

	<div class="bg-drophb hidden absolute w-52">
		<slot name="dropcontent" />
	</div>
</div>

<style>
  div:hover > div{
    display:block;
    outline-style: solid;
    outline-width: 1px;
  }

  div:hover > a[class="!active"]{
    background: #708787;
    color: #d6cecc;
  }
</style>