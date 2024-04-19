<script lang="ts">
  import { onMount } from "svelte";
  import { title } from "$lib/stores.js";

  onMount(() => {
    $title = "Contact Us";
  })
</script>

<p>Contact us</p>
