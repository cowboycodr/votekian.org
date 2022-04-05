<script>
  import Heading from "$lib/components/Heading.svelte";
  import Link from "$lib/components/Link.svelte";
</script>

<div class="container">
    <p>vote</p>
    <Heading>INGRID BLAKETER</Heading>
    <p>for '23 class president</p>
    <div style="font-size: .9rem; text-align: center;">
      <Link href="/campaign/why_im_not_running">Why I dropped out of the running?</Link>
      <Link href="/campaign">Old website</Link>
    </div>
</div>

<style>
  .container {
    position: absolute;

    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  p {
    font-size: 1.3em;
    text-align: center;
  }

  p:first-of-type {
    margin-bottom: .2em;
  }

  p:last-of-type {
    margin-top: .2em;
  }
  
  a {
    text-align: center;

    color: rgba(0, 149, 255, 0.6);
  }
</style>