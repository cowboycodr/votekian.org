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
  }

  a:hover {
    background-size: 100% 100%;
    color: var(--secondary-color);

    transition: color 400ms;
    transition: background-size 400ms;
  } 
</style>