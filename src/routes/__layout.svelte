<main>
    <slot></slot>
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
    --max-width: 1080px;

    min-width: 414px;
  }

  :global(:root) {
  --primary-color: #ffffff;
  --secondary-color: #000;
  --accent-color: #969696;
  }

  :global(section) {
    margin: 5%;
    padding-bottom: 1%;
    border-bottom: 1px solid var(--accent-color);
  }

  .container {
    max-width: var(--max-width);
    min-height: 100vh;
    margin: auto;
  }
</style>