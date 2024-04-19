<script lang="ts">
  import { push, link, location } from 'svelte-spa-router';

  const links = [
    { name: "Menu", link: "/#/" }, 
    { name: "Bugger Night", link: "/#/bugger-night" }, 
    { name: "Accomodation", link: "/#/accomodation" }, 
    { name: "Camp Ground", link: "/#/camp-ground" },
    { name: "Events", link: "/#/events" },
  ]
</script>

<div id="navbar">
  <div id="deer-wrapper">
    <img src="/photos/deer.png" alt="A deer silhouette" />
  </div>
  <div id="leftlogo"></div>
  <div id="textlogo">
    <h1><a href="/#/">The<br>Pelorus<br>Tavern</a></h1>
  </div>
  <div class="links">
  {#each links as link}
    <div class="link-wrapper">
      <a class:color={"/#" + $location == link.link} href={link.link}>{link.name}</a>
    </div>
  {/each}
  </div>
  <div class="book-button-wrapper">
    <button on:click={(e) => {push("/contact-us")}}>CONTACT US</button>
  </div>
</div>

<style lang="scss">
  #navbar {
    display: flex;
    align-items: center;
    position: fixed;
    top: 0;
    left: 0;
    width: 98%;
    height: 100px;
    z-index: 1;
    background-color: white;
    border-bottom: 1px solid black;
    box-shadow: 0 5px #fff;
    margin-left: 1%;
    margin-right: 1%;
    margin-bottom: 5px;
  }

  #leftlogo {
    border-left: 1px solid black;
    height: 60px;
    margin-left: 10px;
    margin-right: 10px;    
    object-fit: cover;
  }

  #textlogo {
    height: 62px;
    width: 100px;
    font-size: 11px;
    line-height: 1.5em;
  }

  h1, div, a {
    font-family: Arial,Helvetica,sans-serif;
  }

  h1 {
    margin-top: 7px;
    font-weight: 200;
  }

  img {
    height: 100%;
    width: 100%;
  }

  #deer-wrapper {
    height: 62px;
    margin-left: 15px;
    object-fit: cover;
  }

  a {
    text-decoration: none;
    color: black;
  }
  .color {
    color: rgb(201,178,0);
  }

  .links {
    margin-left: auto;
    margin-right: 0;
    display: flex;
    align-items: center;
  }

  .link-wrapper {
    margin-left: 10px;
    margin-right: 10px;
    font-family: 'open sans', sans-serif;

    :hover {
      color: rgb(134,119,0);
      transition: color 400ms;
    }
  }

  .book-button-wrapper {
    margin-left: 10px;
    margin-right: 20px;
  }

  button {
    margin: 0;
    color: black;
    background-color: transparent;
    border-radius: 0;
    height: 40px;
    border: 1px solid black;
    font-family: 'open sans', sans-serif;
    font-weight: 400;
    padding-left: 15px;
    padding-right: 15px;
    transition: background-color 400ms, color 400ms;
  }

  button:hover {
    background-color: black;
    color: white;
    transition: background-color 400ms, color 400ms;
  }
</style>
