<script lang="ts">
  import { slide } from 'svelte/transition';
  import { sineInOut } from 'svelte/easing';
  export let name:string, id:string;

	// Close the dropdown if the user moves the cursor outside of it
  function remove(id:string): void {
    var Dropbutton = document.getElementById('Dropbutton'+id);

    if (visible) {  
      visible = false;

      setTimeout(() => {Dropbutton.classList.remove('bg-hoverhb', 'text-hoverhf');}, 300);
    } else {
      Dropbutton.classList.remove('bg-hoverhb', 'text-hoverhf');
    }
  }

  // Lets the button stay highlighted while in the menu
  function hover(id:string): void {
    var Dropbutton = document.getElementById('Dropbutton'+id);
    Dropbutton.classList.add('bg-hoverhb', 'text-hoverhf');
  }

  let visible = false;
</script>

<div class="float-left overflow-hidden text-mainhf" on:mouseleave={() => {remove(id)}} on:mouseenter={() => {hover(id)}}>
  <button class="dropbtn cursor-pointer border-none outline-none px-4 py-1 rounded-md flex items-center m-0 transition duration-300 ease-out" on:click={() => {visible = !visible}} id="Dropbutton{id}">
    <slot name="img"/>
    <div class="pl-4">&#8192;| {name}</div>
  </button>
  {#if visible}
  <div class="absolute bg-drophb min-w-[200px] shadow-md z-[1] rounded-md" transition:slide={{ duration: 300, easing: sineInOut }} id="Dropdown{id}">
    <slot name="dropcontent"/>
  </div>
  {/if}
</div>