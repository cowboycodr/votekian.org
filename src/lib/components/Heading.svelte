<script>
  export let tag;
</script>

<h1 id={tag}><slot></slot></h1>

<style>
  h1 {
    font-size: 5rem;
    font-weight: 700;

    margin-top: 0px;
    margin-bottom: 0px;
    margin-left: -5px;

    line-height: 75%;

    overflow-wrap: break-word;

    -webkit-hyphens: auto;
    -moz-hyphens: auto;
    hyphens: auto;

    /* background-image: url(/images/flag.jpg);
    background-repeat: no-repeat;
    background-clip: text;
    background-size: 100%;
    background-position-x: -10px;

    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;

    text-shadow: -3px -3px var(--secondary-color); */

    filter: drop-shadow(2px 0px 1px #FD3E3E) drop-shadow(-2px -2px 1px #4DE8F4);
  }
</style>