<script lang="ts">
  import { page } from '$app/stores';
  export let path: string, name;
</script>

<a href={path} class="px-4 py-1 flex items-center hover:bg-hoverhb hover:text-hoverhf transition duration-300 ease-out">
  <slot name="img"/>&#8192;| {name}</a>