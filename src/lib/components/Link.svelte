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
    text-decoration: none;
    color: var(--secondary-color);

    background-image: linear-gradient(var(--secondary-color), var(--secondary-color));
    background-size: 0% 100%;
    background-repeat: no-repeat;
    background-position: left bottom;

    transition: color 400ms;
    transition: background-size 400ms;
  }

  a:hover {
    background-size: 100% 100%;
    color: var(--primary-color);

    transition: 400ms;
  } 
</style>