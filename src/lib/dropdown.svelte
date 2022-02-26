<script lang="ts">
  import { slide, fade } from 'svelte/transition';
  import { sineInOut } from 'svelte/easing';
  export let name:string;

  let visible = false;  // dropcontent visibility
  let hover = false;    // button hover active
  let hovering = false; // menu hovering
</script>

<div class="float-left overflow-hidden text-mainhf" on:mouseleave={() => {if (!visible) {hover = false}; visible = false; hovering = false}} on:mouseenter={() => {hover = true; hovering = true}}>
  <button class="{hover == true ? "bg-hoverhb text-hoverhf" : ""} dropbtn cursor-pointer border-none outline-none px-4 py-1 rounded-md flex items-center m-0 transition duration-300 ease-in-out" on:click={() => {visible = !visible}}>
    <div class="hidden md:flex md:items-center md:justify-center md:w-5">
      {#if !visible}
        <slot name="img1"/>
      {:else}
      <slot name="img2"/>
      {/if}
    </div>
    <div class="hidden md:flex">&#8192;|&#8192;</div> 
    <div>{name}</div>
  </button>
  {#if visible}
  <div class="absolute bg-drophb min-w-[200px] shadow-md z-[1] rounded-md" transition:slide={{ duration: 300, easing: sineInOut }} on:outroend={() => {if (!hovering) {hover = false}}}>
    <slot name="dropcontent"/>
  </div>
  {/if}
</div>