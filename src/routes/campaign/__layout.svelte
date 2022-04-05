<script>
  import { slide } from "svelte/transition";

  // votekian.org default look
  import Header from "$lib/campaign/components/Header.svelte";
  import Footer from "$lib/campaign/components/Footer.svelte";

  let showEndorsement = true;
</script>

{#if showEndorsement}
<div 
  out:slide={{duration: 200}}
  class="endoresement"
>
  <p>
    Kian has dropped out of the election.
    Please review <a href="/" sveltekit:prefetch>this</a> for 
    campaign and endoresement information.
  </p>
  <span class="close" on:click={() => {showEndorsement = false}}>
    <svg xmlns="http://www.w3.org/2000/svg" width="10" height="10" viewBox="0 0 24 24">
      <path d="M24 20.188l-8.315-8.209 8.2-8.282-3.697-3.697-8.212 8.318-8.31-8.203-3.666 3.666 8.321 8.24-8.206 8.313 3.666 3.666 8.237-8.318 8.285 8.203z"/>
    </svg>
  </span>
</div>
{/if}
<Header />
<main>
  <div class="container">
    <slot></slot>
  </div>
</main>
<Footer />

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@500;700&family=Rubik:wght@300;400&display=swap');
  :global(*) {
    font-family: "Roboto", sans-serif;
    color: var(--secondary-color);

    transition: background-color 400ms;
  }

  :global(body) {
    margin: 0;
    background-color: var(--primary-color);
    --max-width: 1080px;

    min-width: 414px;
  }

  :global(:root) {
  --primary-color: #ffffff;
  --secondary-color: #000;
  --accent-color: #969696;
  }

  :global(.dark) {
    --primary-color: #000;
    --secondary-color: #fff;
    --accent-color: #969696;
  }

  :global(section) {
    margin: 5%;
    padding-bottom: 1%;
    border-bottom: 1px solid var(--accent-color);
  }

  .endoresement {
    display: flex;
    align-items: center;

    height: 2em;
    background-color: red;
  }

  .endoresement p {
    margin-top: 0;
    margin-bottom: 0;

    color: white;
  }

  span.close {
    width: 20px;
    height: 20px;

    fill: white;
    padding-right: 10px;

    margin-left: auto;

    cursor: pointer;
  }

  .container {
    max-width: var(--max-width);
    min-height: 100vh;
    margin: auto;
  }

  a {
    color: rgba(0, 149, 255, 0.8);
  }
</style>