<script>
  export let content = "bleep";

  function sensorContent(content) {
    let result = content[0];

    for (let i = 0; i < content.length - 2; i++) {
      result += "*"
    }

    result += content[content.length - 1];
    return result;
  } 

  let sensoredContent = sensorContent(content);

  function handleMouseEnter() {
    sensoredContent = content;
  }

  function handleMouseLeave() {
    sensoredContent = sensorContent;
  }
</script>

<span
  class="censored"
  on:mouseenter={() => {sensoredContent = content}}
  on:mouseleave={() => {sensoredContent = sensorContent(content)}}
>
  {sensoredContent}
</span>

<style>
  .censored {
    color: var(--primary-color);

    background-image: linear-gradient(var(--secondary-color), var(--secondary-color));
    background-size: 100% 100%;
    background-repeat: no-repeat;
  }

  .censored:hover {
    color: var(--secondary-color);
    background-size: 0% 100%;

    transition: 400ms;
  }
</style>