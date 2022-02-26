<script lang="ts">
  import { page } from '$app/stores';
  export let path: string, name;
</script>

<a href={path} class="{$page.url.pathname == path ? "bg-mainhb text-hoverhf group-hover:bg-hoverhb group-hover:text-mainhf" : "text-mainhf"} px-4 py-1 rounded-md flex items-center  hover:bg-hoverhb hover:text-hoverhf transition duration-300 ease-out">
  <div class="hidden md:flex md:items-center md:justify-center"><slot name="img"/></div>
  <div class="hidden md:flex">&#8192;|&#8192;</div> 
  <div>{name}</div>
</a>