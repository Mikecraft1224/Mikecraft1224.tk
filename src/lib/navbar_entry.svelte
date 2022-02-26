<script lang="ts">
  import { page } from '$app/stores';
  export let path: string, name;
</script>

<a href={path} class="{$page.url.pathname == path ? "bg-mainhb text-hoverhf group-hover:bg-hoverhb group-hover:text-mainhf" : "text-mainhf"} px-4 py-1 rounded-md flex items-center  hover:bg-hoverhb hover:text-hoverhf transition duration-300 ease-out">
  <slot name="img"/>
  <div class="pl-4">&#8192;| {name}</div>
</a>