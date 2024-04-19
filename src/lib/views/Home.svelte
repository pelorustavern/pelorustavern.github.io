<script lang="ts">
  import MarkdownComponent from "$lib/components/MarkdownComponent.svelte";
  import menuMarkdown from "$lib/Menu.md?raw";
  import takeawayMarkdown from "$lib/Takeaway.md?raw";
  import { onMount } from "svelte";
  import { title } from "$lib/stores.js";

  onMount(() => {
    $title = "";
  })
</script>

<div id="wrapper">
  <div id="heading">
    <div id="menuDiv">
      <h1>Menu</h1>
      <p style="font-style: italic; font-size: 11px">All takeaway items are also available in house </p>
    </div>
  </div>
  <div></div>
  <div class="blackbox">
    <div class="box-heading">
      <h1 style="margin: 0 20px 20px 20px; padding-top: 20px">In House</h1>
    </div>
    <div style="padding: 0 20px 20px 20px">
      <MarkdownComponent source={menuMarkdown}></MarkdownComponent>
    </div>
  </div>
  <div></div>
  <div class="blackbox">
    <div class="box-heading">
      <h1 style="margin: 0 20px 20px 20px; padding-top: 20px">Takeaway</h1>
    </div>
    <div style="padding: 0 20px 20px 20px">
      <MarkdownComponent source={takeawayMarkdown}></MarkdownComponent>
    </div>
  </div>
</div>

<style>
  #heading {
    background-color: black;
    color: white;
    align-items: baseline;
    justify-content: end;
    height: 100%;
    border: 1px solid black;
  }

  h1 {
    font-weight: 300;
    font-size: 50px;
    font-family: 'open-sans', sans-serif;
    font-stretch: condensed;
    letter-spacing: -3px;
    width: 100%;
    padding-left: auto;
  }

  #wrapper {
    padding-top: 40px;
    padding-bottom: 40px;
    display: grid;
    grid-template-columns: 30% 3% 32% 3% 32%;
    align-items: center;
  }

  #menuDiv {
    position: sticky;
    top: 120px;
    margin: 20px;
  }

  .box-heading {
    position: sticky;
    top: 105px;
    z-index: 1;
    background-color: white;
  }

  .box-heading::after {
    content: "";
    position: absolute;
    inset: 0;
    z-index: -1;
    mask: linear-gradient(to top, transparent, black 35%);
    backdrop-filter: blur(10px);
    height: 135px;
  }
</style>
