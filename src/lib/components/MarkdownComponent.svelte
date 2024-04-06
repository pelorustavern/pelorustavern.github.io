<script lang="ts">
  import SvelteMarkdown from 'svelte-markdown'
  export let source;
</script>

<SvelteMarkdown {source} />

<style>
  h3 {
    font-weight: 200;
  }
</style>
