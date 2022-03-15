
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
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@500;700&family=Rubik:wght@300;400&display=swap');
  :global(*) {
    font-family: "Roboto", sans-serif;
    color: var(--secondary-color);

    transition: background-color 400ms;
  }

  :global(body) {
    margin: 0;
    background-color: var(--primary-color);
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