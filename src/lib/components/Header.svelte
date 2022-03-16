<script>
  import { afterUpdate } from "svelte/internal";

  import Link from "./Link.svelte";

  import Toggle from "svelte-toggle";
  import DarkMode from "svelte-dark-mode";

  let switchColor = "black";
  let toggledColor = "white";
  let untoggledColor = "black";

  let theme;
  let toggled;

  afterUpdate(() => {
    document.body.className = theme;
    
    toggled = theme == "dark" ? true : false;

    setInterval(() => {
      toggled = !toggled;
    }, 50)
  })

  function switchColors(theme) {
    if (theme === "light") {
      switchColor = "white";
      toggledColor = "black";
      untoggledColor = "black";
    } else {
      switchColor = "black";
      toggledColor = "white";
      untoggledColor = "white";
    }
  }

  let scrolled = false;
  function handleScroll() {
    scrolled = document.documentElement.scrollTop > 0;
  }

  $: theme = toggled ? "dark" : "light";
  $: switchColors(theme)
</script>

<DarkMode bind:theme />

<svelte:window 
  on:scroll={handleScroll}
/>

<div 
  class="container"
>
  <div class="header">
    <span class="home">
      <Link>votekian.org</Link>
    </span>
    <span class="grouped">
      <Link href="/why">why</Link>
      <Toggle 
        small 
        hideLabel
        {switchColor}
        {toggledColor}
        {untoggledColor}
        bind:toggled
      />
    </span>
  </div>
</div>

<style>
  .header {
    display: flex;
    justify-content: space-between;
    margin: auto;

    max-width: var(--max-width);
    padding: 15px;
  }

  .container {
    position: sticky;
    top: 0;

    background-color: var(--primary-color);
    border-bottom: 1px solid var(--accent-color);

    z-index: 9999;
  }

  .grouped {
    display: flex;
    justify-content: space-between;

    width: 10%;
    min-width: 50px;
    max-width: 100px;
  }

  :global(.grouped * + *) {
    margin-left: 5px;
  }
</style>