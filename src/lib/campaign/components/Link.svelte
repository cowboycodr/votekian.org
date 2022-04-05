<script>
  export let href = "/";
</script>

<a 
  sveltekit:prefetch 
  {href}
>
  <slot></slot>
</a>

<style>
  a {
    padding: 1px;
    text-decoration: none;
    color: var(--primary-color);
    background-color: var(--secondary-color);

    background-image: linear-gradient(var(--primary-color), var(--primary-color));
    background-size: 0% 100%;
    background-repeat: no-repeat;
    background-position: left bottom;

    transition: color 400ms;
    transition: background-size 400ms;

    filter: drop-shadow(2px 0px 1px #FD3E3E) drop-shadow(-2px -2px 1px #4DE8F4);
  }

  a:hover {
    background-size: 100% 100%;
    color: var(--secondary-color);
    filter: drop-shadow(-2px -2px 3px #FD3E3E) drop-shadow(2px 0px 3px #4DE8F4);

    transition: 400ms;
  } 
</style>