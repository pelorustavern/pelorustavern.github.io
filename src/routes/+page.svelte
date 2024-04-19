<script lang="ts">
  import Navbar from "$lib/components/Navbar.svelte";
  import Events from "$lib/views/Events.svelte";
  import NotFound from "$lib/views/NotFound.svelte";
  import CampGround from "$lib/views/CampGround.svelte";
  import Accomodation from "$lib/views/Accomodation.svelte";
  import BuggerNight from "$lib/views/BuggerNight.svelte";
  import Home from "$lib/views/Home.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import ContactUs from "$lib/views/ContactUs.svelte";
  import Redirect from "$lib/views/Redirect.svelte";
  import ComingSoon from "$lib/views/ComingSoon.svelte";
  import Router from 'svelte-spa-router';
  import { title } from "$lib/stores.js";

  const routes = {
    "/": Home,
    "/bugger-night": ComingSoon,
    "/accomodation": ComingSoon,
    "/camp-ground": ComingSoon,
    "/events": ComingSoon,
    "/contact-us": ComingSoon,
    "/#/*": Redirect,
    "*": NotFound,
  }

  $: titleD = $title + ($title == "" ? "" : " | ") + "The Pelorus Tavern"
</script>

<svelte:head>
  <title>{titleD}</title>
</svelte:head>

<Navbar />
<div style="position: relative; top: 100px; width: 90%; margin-left: 5%; margin-right: 5%">
  <Router {routes} />
</div>
<div style="position: relative; margin-top: auto">
  <Footer/>
</div>

<style lang="scss">
  :global(.blackbox) {
    border: 1px solid black;
    border-radius: 0;
    align-self: stretch;
  }

  :global(*) {
    margin: 0;
    padding: 0;
  }
</style>
