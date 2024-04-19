<script lang="ts">
  import { onMount } from "svelte";
  import { title } from "$lib/stores.js";

  onMount(() => {
    $title = "Camp Ground";
  })
</script>

<p>Camp Ground</p>
