<script>
  import Heading from "$lib/components/Heading.svelte";

  let message = '';

  setInterval(function() {
    message += "sdijfsdlfsmdfklsdfmsdljkfsmdfksdfslkdjnfsdfslkjdfnskljdfnsdkjfnsdlknskldjfnksjdfnsdfnslkdfsnldf" + 1;
    message + 1
  }, 1)
</script>

<div class="container">
    <div style="text-align: center;">
      <Heading tag="endorsement">LEAVE</Heading>
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