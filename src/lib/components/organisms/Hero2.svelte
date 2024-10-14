<script>
  import { Button, ArrowRight, RouteIcon, CocktailIcon } from '$lib/index'
  // export let items
</script>

<section>
  <video
    autoplay
    loop
    muted
    width="1280"
    height="1000"
    aria-label=""
    aria-hidden="true"
    poster="/hero-image-background.webp"
  >
    <!-- <source src="" type="video/webm" />
    <source src="" type="video/webm" />
    <source src="path/to/video-480p.mp4" type="video/mp4" media="(min-width: 480px)" />
    <source src="path/to/video-360p.mp4" type="video/mp4" media="(max-width: 1280px)" /> -->
  </video>
  <div class="overlay"></div>
  <article class="hero-content">
    <h1>
      GROEPSBOEKING
    </h1>
    <div class="hero-description">
      <p>Bedrijfsuitje, vrijgezellenfeest of vriendenactiviteit? De Cocktail Walk past perfect bij jou.</p>
      <Button
        variant="primary"
        title="book now"
        icon={ArrowRight}
        iconColor="var(--btn-primary-text-clr)"
        size="lg"
      />
    </div>
  </article>
</section>
<section>
  <div>
    <article>
      <p><span><RouteIcon width="25" height="25" fill="var(--page-bg-color)" /></span>Amstedam & Rottedam</p>
      <p><span><CocktailIcon width="25" height="25" fill="var(--page-bg-color)" /></span>3 Cocktails</p>
      <p><span><CocktailIcon width="25" height="25" fill="var(--page-bg-color)" /></span>3 Barreseveringen</p>
      <p><span><CocktailIcon width="25" height="25" fill="var(--page-bg-color)" /></span>7 Dagen per week</p>
    </article>
    <article>
      <p><span><RouteIcon width="25" height="25" fill="var(--page-bg-color)" /></span>Zelfgeleide tour van 3-4 uur</p>
      <p><span><CocktailIcon width="25" height="25" fill="var(--page-bg-color)" /></span>Groepsgroottes 6-30 personen</p>
      <p><span><CocktailIcon width="25" height="25" fill="var(--page-bg-color)" /></span>Gepersonaliseerde kaart & routes mogelijk</p>
      <p><span><CocktailIcon width="25" height="25" fill="var(--page-bg-color)" /></span>Snacks mogelijk</p>
    </article>
  </div>
</section>

<style>
  section {
    padding-inline: 2em;
  }

  section:nth-of-type(1) {
    display: grid;
    position: relative;
    height: 55vh;
    overflow: hidden;
    align-items: center;
  }
  section:nth-of-type(1) > article {
    max-width: 90em;
    margin: auto;
    width: 100%;
  }

  section:nth-of-type(2) {
    background-color: var(--accent1-secondary);
    padding-block: 2em;
  }

  section:nth-of-type(2) > div {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    max-width: 90em;
    margin: auto;
  }

  section:nth-of-type(2) > div > article {
    display: flex;
    flex-direction: column;
    gap: 1em;
  }

  section:nth-of-type(2) > div:first-of-type {
    margin-bottom: 1em;
  }

  video {
    position: absolute;
    top: 50%;
    left: 50%;
    width: auto;
    height: 100%;
    transform: translate(-50%, -50%);
    min-width: 100%;
    min-height: 100%;
    object-fit: cover;
    opacity: 0.8;
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 1;
  }

  .hero-content {
    font-weight: 700;
    color: #fff;
    z-index: 1;
  }

  .hero-description > p {
    padding: 0.5em;
  }

  h1 {
    position: relative;
    display: inline-block;
    text-align: center;
    width: 100%;
    margin-bottom: 2em;
    font-weight: 700;
    font-size: clamp(2.648rem, 6vw, 4.241rem);
    letter-spacing: -1px;
    filter: drop-shadow(0 0 0.4rem #000);
    animation: heading;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  @keyframes heading {
    0% {
      top: -200px;
    }
    100% {
      top: -2px;
    }
  }

  p {
    font-size: 1.2rem;
    font-weight: 700;
    position: relative;
    animation-name: content;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }

  @keyframes content {
    0% {
      left: -1000px;
    }
    100% {
      left: 0px;
    }
  }

  @media (min-width: 30em) {
    section:nth-of-type(1) {
      height: 70vh;
    }

    .hero-description {
      max-width: 45rem;
    }
    .hero-description > p {
      max-width: 75%;
    }
  }
  @media (min-width: 44em) {
    section:nth-of-type(2) > div {
      flex-direction: row;
    }
    p {
      font-size: 1.5em;
    }
    section:nth-of-type(2) > div:first-of-type {
    margin-bottom: 0;
    }
  }

  @media (min-width: 55em) {
    section {
      padding-inline: 8em;
    }
  }
</style>
