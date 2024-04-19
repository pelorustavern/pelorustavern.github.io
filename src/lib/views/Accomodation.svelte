<script lang="ts">
  import { onMount } from "svelte";
  import { title } from "$lib/stores.js";

  onMount(() => {
    $title = "Accomodation";
  });
</script>

<p>Accomodation</p>
