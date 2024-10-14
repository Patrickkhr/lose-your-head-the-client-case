<script>
  // export let items
  import { CocktailIcon } from '$lib/index'
  import logo from '$lib/assets/logo.webp'
</script>

<section>
  <form method="post" action="/"  class="">
    <h1>Boeken</h1>
    <div class="">
      <label for="first-name">Voornaam:</label>
      <input type="text" name="first-name" id="first-name" required />
    </div>
    <div class="">
      <label for="last-name">Achternaam:</label>
      <input type="text" name="last-name" id="last-name" required />
    </div>
    <div class="">
      <label for="email">Enter your email: </label>
      <input type="email" name="email" id="email" required />
    </div>
    <div class="">
      <label for="phone">Telefoonnummer:</label>
      <input type="tel" name="phone" id="phone" required />
    </div>
    <div class="">
      <label for="persons">Hoeveel personen?</label>
      <input type="text" name="persons" id="persons" required />
    </div>
    <div class="">
      <label for="request">Aanvraag:</label>
      <textarea id="story" name="story"></textarea>
    </div>
    <div class="">
      <label for="date">Datum:</label>
      <input type="date" name="date" id="date" required />
    </div>
    <div class="">
      <label for="time">Choose a time for your meeting:</label>
      <input type="time" name="time" id="time" min="09:00" max="22:00" value="14:30" required />
    </div>
    <div class="">
      <button type="submit">Verstuur</button>
    </div>
  </form>
  <article>
    <div>
      <img src={logo} height="150" width="150" alt="Wogo Logo" />
    </div>
    <div>
      <p><span><CocktailIcon width="25" height="25" fill="white" /></span>3 Cocktails</p>
      <p><span><CocktailIcon width="25" height="25" fill="white" /></span>3 Cocktails</p>
    </div>
      <ul class="social-media-list" role="list" aria-label="Social links">
        <li>
            <a href="/">
              <img src={logo} height="50" width="50" alt="Wogo Logo" loading="lazy" />
            </a>
        </li>
        <li>
          <a href="/">
            <img src={logo} height="50" width="50" alt="Wogo Logo" loading="lazy" />
          </a>
        </li>
        <li>
          <a href="/">
            <img src={logo} height="50" width="50" alt="Wogo Logo" loading="lazy" />
          </a>
        </li>
      </ul>
  </article>
</section>

<style>

  section {
    padding-inline: 2em;
    display: flex;
    flex-direction: column;
    gap: 3em;
    padding-block: 4em;
    max-width: 90em;
    margin: auto;
  }
  
  form {
    display: flex;
    flex-direction: column;
    gap: 1em;
    position: relative;
    padding: 2em;
  }

  form::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    background-color: #3F2B21;
    border-radius: 8px;
    z-index: -1;
    box-shadow: 0px 4px 0px rgba(0, 0, 0, 0.25);
  }

  form > div {
    display: flex;
    flex-direction: column;
  }

  form > div > input,
  form > div > textarea {
    width: 100%;
    padding: 0.625em;
    border: none;
    border-radius: 5px;
    background-color: #fff;
    color: #000;
  }

  form label, h1 {
    color: white;
  }

  form > h1 {
    font-size: var(--fs-2xl);
  }


  button {
    background-color: #f7956f;
    border: none;
    padding: 1em;
    color: white;
    cursor: pointer;
    border-radius: 5px;
  }

  article, div {
    display: flex;
    flex-direction: column-reverse;
    gap: 1em;
  }

  article > div,
  article > ul > li {
    background-color: #3F2B21;
    border-radius: 8px;
    box-shadow: 0px 4px 0px rgba(0, 0, 0, 0.25);
  }

  article > div:nth-of-type(1) {
    align-items: center;
    padding: 3em;
  }

  article > div:nth-of-type(2) {
    padding: 1em;
  }
  article > div:nth-of-type(2) > p {
    display: flex;
    gap: 1em;
    align-items: center;
  }

  article > ul {
    display: flex;
    justify-content: space-between;
    list-style-type: none;
    gap: 0.5em
  }

  article > ul > li {
    background-color: #3F2B21;
    border-radius: 8px;
  }

  article > ul > li > a {
    display: flex;
    align-items: center;
    height: 100%;
    width: 100%;
    padding: 1em;
  }

  @media (min-width: 30em) {

  }

  @media (min-width: 44em) {
    section {
      flex-direction: row;
      justify-content: space-between;
    }
    form {
      width: 50%;
      max-width: 50%;
    }
    article {
      flex-direction: column;
    }
    
  }

  @media (min-width: 55em) {
    section {
      padding-inline: 8em;
    }
  }
</style>
