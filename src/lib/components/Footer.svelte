<script lang="ts">
  import { push } from "svelte-spa-router";
</script>

<div id="wrapper">
  <p>21 Wakamarina Road, Canvastown,<br>Havelock 7178  |  <strong>03 5742888</strong></p>
  <div id="contact-wrapper">
    <a href="https://www.facebook.com/p/Pelorus-Tavern-Trout-Hotel-100089879629385/" id="facebook">
      <svg fill="#000000" height="30px" width="30px" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 310 310" xml:space="preserve"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g id="XMLID_834_"> <path id="XMLID_835_" d="M81.703,165.106h33.981V305c0,2.762,2.238,5,5,5h57.616c2.762,0,5-2.238,5-5V165.765h39.064 c2.54,0,4.677-1.906,4.967-4.429l5.933-51.502c0.163-1.417-0.286-2.836-1.234-3.899c-0.949-1.064-2.307-1.673-3.732-1.673h-44.996 V71.978c0-9.732,5.24-14.667,15.576-14.667c1.473,0,29.42,0,29.42,0c2.762,0,5-2.239,5-5V5.037c0-2.762-2.238-5-5-5h-40.545 C187.467,0.023,186.832,0,185.896,0c-7.035,0-31.488,1.381-50.804,19.151c-21.402,19.692-18.427,43.27-17.716,47.358v37.752H81.703 c-2.762,0-5,2.238-5,5v50.844C76.703,162.867,78.941,165.106,81.703,165.106z"></path> </g> </g></svg>
    </a>
    <div id="contact-separator"></div>
    <div id="contact-button">
      <button on:click={(e) => push("/contact-us")}>Contact us</button>
    </div>
  </div>
  <p style="font-size: 11px; margin-top: 10px">© 2024 The Pelorus Tavern and <a style="color: black" href="https://github.com/PelorusTavern/pelorustavern.github.io">GitHub</a> contributors - Made with ♡ </p>
</div>

<style>
  #wrapper {
    border-top: 1px solid black;
    width: 90%;
    margin: 105px 5% 0 5%;
    padding-top: 15px;
    padding-bottom: 30px;
    position: sticky;
    bottom: 0;
  }

  p {
    font-family: 'open-sans';
    font-size: 14px;
    font-weight: 400;
  }

  strong {
    font-weight: 450;
  }

  #contact-wrapper {
    display: flex;
    margin-top: 30px;
  }

  #contact-separator {
    height: 100%;
    border-left: 1px solid black;
    height: 30px;
    margin-left: 18px;
    margin-right: 25px;
  }

  button {
    height: 28px;
    border: 1px solid black;
    color: white;
    background-color: black;
    font-family: 'open-sans', sans-serif;
    border-radius: 0;
    padding-left: 20px;
    padding-right: 20px;
    margin-top: 1px;
    font-size: 14px;
    transition: color 400ms, background-color 400ms;
  }

  button:hover {
    background-color: white;
    color: black;
    transition: color 400ms, background-color 400ms;
  }
</style>
