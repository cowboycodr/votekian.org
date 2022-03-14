<script context="module">
  export const prerender = true;

  export function load({ error, status }) {
    return {
      props: {
        status: status,
        errorMessage: error.message,
      }
    }
  }
</script>

<script>
  export let status;
  export let errorMessage;
</script>

<div class="container">
  <div class="error">
      <h1>
        {status}
      </h1>
    <p
      on:click={() => {navigator.clipboard.writeText(errorMessage)}}
    >
      {errorMessage}
    </p>
  </div>
</div>

<style>
  .container {
    position: relative;

    width: 100%;
    height: 100vh;
  }

  .error {
    position: absolute;
    
    top: 50%;
    left: 50%;

    transform: translate(-50%, -50%);
  }

  h1 {
    font-size: 7rem;
    width: min-content;
    padding: 0;
    margin: 0;
    padding-left: 0.1em;
    padding-right: 0.1em;
    margin-bottom: 3px;

    background-image: linear-gradient(red, red);
    background-size: 0.1em 100%;
    background-repeat: no-repeat;
  }

  h1:hover {
    background-size: 100% 100%;
    transition: 400ms;
    color: white;
  }

  p {
    cursor: copy;
  }
</style>