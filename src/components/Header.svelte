<script>
  import { fly } from "svelte/transition";
  export let visible;
</script>

<style>
</style>

<header class="header">
  <label> <input type="checkbox" bind:checked={visible} /> visible </label>
  {#if visible}
    <p transition:fly={{ x: -200, duration: 2000 }}>Flies in and out</p>
  {/if}
</header>
