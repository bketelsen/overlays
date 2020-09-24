<script>
  import { fly } from "svelte/transition";
  export let visible;
</script>

<style>
  @import url(https://fonts.googleapis.com/css?family=Open+Sans:400,300);
  @import url(https://fonts.googleapis.com/css?family=Arimo:400,700);

  .animation {
    width: 20em;
    height: 4em;
    margin: 1em auto;
    position: relative;
  }

  .arimo {
    font-family: Arimo;
  }

  .red {
    color: #cf4c4e;
  }

  .white {
    color: white;
  }

  .light {
    font-weight: 300;
  }

  .bold {
    font-weight: 700;
  }

  .mask {
    overflow: hidden;
    position: relative;
  }
</style>

<footer class="footer">
  <label> <input type="checkbox" bind:checked={visible} /> visible </label>
  {#if visible}
    <div id="animation-2" class="animation">
      <div class="red bold arimo mask">
        <div>John Doe</div>
      </div>
      <div class="white light mask">
        <div>Motion Designer</div>
      </div>
    </div>
  {/if}
</footer>
<!-- .footer -->
