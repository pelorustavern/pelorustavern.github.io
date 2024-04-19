<script lang="ts">
  import { onMount } from "svelte";
  import { title } from "$lib/stores.js";

  onMount(() => {
    $title = "Bugger Night";
  })
</script>

<p>BuggerNight</p>
