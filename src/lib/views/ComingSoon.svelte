<script lang="ts">
  import { onMount } from "svelte";
  import { title } from "$lib/stores.js";

  onMount(() => {
    $title = "";
  });
</script>

<div id="wrapper">
  <p>Coming soon...</p>
</div>

<style>
  #wrapper {
    height: 400px;
    padding: 20px;
  }

  p {
    font-family: 'open-sans', sans-serif;
    font-size: 50px;
    font-style: italic;
    character-spacing: condensed;
    font-weight: 200;
  }
</style>
