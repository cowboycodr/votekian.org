<svelte:head>
  <title>votekian.org</title>
</svelte:head>

<section>
  <p>
    vote
  </p>
  <h1 class="name">
    Kian
  </h1>
  <h1 class="name">
    McKenna
  </h1>
  <p>
    for '23 class president
  </p>
</section>

<style>
  h1.name {
    font-weight: 700;

    margin-left: -5px;
    margin-top: 0px;
    margin-bottom: 0px;
    font-size: 5em;

    line-height: 75%;

    background-image: url(/images/flag.jpg);
    background-repeat: no-repeat;
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-position-x: -10px;
    background-size: 100%;
    text-shadow: -3px -3px var(--secondary-color);
  }

  p {
    font-size: 1.3em;
  }

  p:first-of-type {
    margin-bottom: 0;
  }

  p:nth-of-type(2) {
    margin-top: 0;
  }
</style>