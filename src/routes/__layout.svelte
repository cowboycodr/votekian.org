
<script>
  // votekian.org default look
  import Header from "$lib/components/Header.svelte";
  import Footer from "$lib/components/Footer.svelte";
</script>

<main>
  <Header />
  <div class="container">
    <slot></slot>
  </div>
  <Footer />
</main>

<style>
  :global(*) {
    font-family: "Roboto", sans-serif;
    font-weight: 500;
    color: var(--secondary-color);

    transition: color 400ms;
    transition: background-color 400ms;
  }

  :global(body) {
    margin: 0;
  }

  :global(:root) {
  --primary-color: #ffffff;
  --secondary-color: #000;
  --accent-color: #969696;

  --max-width: 1080px;
  }

  :global(.dark) {
    --primary-color: #000;
    --secondary-color: #fff;
    --accent-color: #969696;
  }

  :global(section) {
    margin: 5%;
    border-bottom: 1px solid var(--accent-color);
  }

  .container {
    max-width: var(--max-width);
    min-height: 100vh;
    margin: auto;
  }
</style>