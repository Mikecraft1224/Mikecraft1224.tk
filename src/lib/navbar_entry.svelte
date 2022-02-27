<script lang="ts">
  import { page } from '$app/stores';
  export let path: string, name;
</script>

<a href={path} class=
    "{$page.url.pathname == path 
      ? "text-mainhoverhf group-hover:text-hoverhf" 
      : "group-hover:text-mainhoverhf "}"
  >
  <div class=
      "{$page.url.pathname == path 
        ? "bg-mainhb group-hover:bg-hoverhb"
        : "hover:bg-hoverhb hover:text-hoverhf"} 
      flex items-center px-4 py-1 rounded-md transition duration-300 ease-out"
    >
    <div class="hidden md:flex md:items-center md:justify-center"><slot name="img"/></div>
    <div class="hidden md:flex">&#8192;|&#8192;</div> 
    <div>{name}</div>
  </div>
</a>