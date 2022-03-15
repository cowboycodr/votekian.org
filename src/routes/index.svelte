<script>
  import Link from "$lib/components/Link.svelte";
  import Heading from "$lib/components/Heading.svelte";
</script>

<svelte:head>
  <title>votekian.org</title>
</svelte:head>

<section>
  <p>
    vote
  </p>
  <Heading tag="name">
    KIAN<br/>MCKENNA
  </Heading>
  <span 
    class="pronouns"
    title="pronouns"
  >
    (yee/haw)
  </span>
  <p>
    for '23 class president
  </p>
</section>
<section>
  <Heading tag="about">ABOUT KIAN</Heading>
  <ul>
    <li>
      6'1" D1 Athlete
    </li>
    <li>
      BACKED BY SMEAST'S FEMINICIST SELF-DEFENSE CLUB
    </li>
    <li>
      <Link href="/why">CLICK HERE FOR MORE INFORMATION 🎯</Link>
    </li>
  </ul>
</section>
<section>
  <Heading tag="accomplishments">
    ACCOMPLISHMENTS
  </Heading>
  <ul>
    <li>
      100+ FORTNITE VICTORY ROYALES
    </li>
    <li>
      SUCCESSFULLY BIRTHED AS NOT ELLEN
    </li>
    <li>
      3 RECOVERIES FROM TRAMATIC BRAIN DAMAGE
    </li>
  </ul>
</section>
<section>
  <Heading tag="plan">MY PLAN</Heading>
  <p class="plan__paragraph">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam, magnam tenetur quis vel itaque tempora accusantium eveniet officia reiciendis provident illum debitis odit pariatur eius suscipit totam nulla excepturi incidunt!
    Vel iusto tempora voluptatibus deleniti inventore molestias vitae nemo obcaecati? Laudantium, aspernatur quisquam. Reiciendis aperiam hic dolore labore quae autem dolorum officia? Hic quam eius illum natus velit quidem officia!
    Repudiandae, modi ut. Fuga officiis, unde laborum autem ex quia ut explicabo recusandae omnis aperiam incidunt iste ea necessitatibus voluptates itaque ducimus. Porro molestias eligendi atque ipsum! Ratione, vitae veritatis?
  </p>
  <br />
  <p class="plan__paragraph">
    Est voluptate enim, necessitatibus voluptatibus ducimus soluta repudiandae, error libero unde vitae vel impedit excepturi quo dicta cumque consectetur labore architecto ullam dolorem, qui possimus sint fuga tenetur dolor. Reprehenderit?
    Corporis vel enim non, molestiae ut corrupti nisi, necessitatibus dolore ratione unde vero architecto perferendis atque nam tempora maiores magni quod qui quam quo dolorum fuga sed ex veniam? Ratione!
    Architecto, est? Nemo ipsum dolorum velit excepturi fugit eligendi neque porro perspiciatis vero aspernatur, incidunt quae suscipit voluptate veniam dolor iste eaque ducimus! Doloremque beatae modi cum porro ex delectus?
    Accusamus optio eius blanditiis commodi ullam excepturi sunt harum quod unde quos! Eum pariatur voluptatum harum adipisci non dignissimos recusandae doloremque quam dolorum reprehenderit dolor, voluptatibus nisi corporis possimus eligendi?
    Expedita et impedit velit doloremque reprehenderit odio quidem quaerat deleniti porro accusantium, eaque eveniet temporibus magnam optio alias obcaecati architecto officiis cupiditate similique fugit rerum. Error iure dolores autem recusandae.
  </p>
  <br />
  <p class="plan__paragraph">
    Quas ab accusamus, velit est unde voluptatum cupiditate illum commodi? Reiciendis, rerum recusandae reprehenderit delectus modi nihil ea aliquam quos quam aspernatur minima libero tempora fuga est voluptas a. Pariatur.
    Fugiat quas maiores harum? Voluptatum dolor, eveniet sed impedit laborum asperiores dolorum explicabo adipisci corrupti assumenda vel blanditiis quibusdam possimus odio dignissimos illum velit, tempora aspernatur cupiditate? Exercitationem, id similique!
  </p>
</section>

<style>
  span.pronouns {
    font-size: .7em;
    color: var(--accent-color);
  }

  p {
    font-size: 1.3em;
  }

  p:first-of-type {
    margin-bottom: 0;
  }

  p {
    margin-top: 0;
  }

  ul li {
    margin: 4px 0;
  }

  p.plan__paragraph {
    margin-left: 1.5em;
    font-size: 1em;
  }
</style>