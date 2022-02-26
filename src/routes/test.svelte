<script>
  let status = true;
</script>

<button on:click={() => {status = !status}}></button>
{#if status}
   <!-- content here -->
{:else}
   <!-- else content here -->
{/if}

<button></button>