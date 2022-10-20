<script>
  import AlpacaImg from './lib/alpaca.svelte';

  let styles = {
    backgrounds: [
      'blue50',
      'blue60',
      'blue70',
      'darkblue30',
      'darkblue50',
      'darkblue70',
      'green50',
      'green60',
      'green70',
      'grey40',
      'grey70',
      'grey80',
      'red50',
      'red60',
      'red70',
      'yellow50',
      'yellow60',
      'yellow70',
    ],
    neck: ['default', 'bend-backward', 'bend-forward', 'thick'],
    ears: ['default', 'tilt-backward', 'tilt-forward'],
    hair: ['default', 'bang', 'curls', 'elegant', 'fancy', 'quiff', 'short'],
    eyes: ['default', 'angry', 'naughty', 'panda', 'smart', 'star'],
    leg: [
      'default',
      'bubble-tea',
      'cookie',
      'game-console',
      'tilt-backward',
      'tilt-forward',
    ],
    mouth: ['default', 'astonished', 'eating', 'laugh', 'tongue'],
    accessories: ['flower', 'earings', 'glasses', 'headphone'],
  };

  let selected_style = '';

  function randomize_alpaca() {
    Object.keys(styles).forEach((e) => {
      alpaca[e] = styles[e][Math.floor(Math.random() * styles[e].length)];
    });
  }

  let alpaca = {};
  randomize_alpaca();
</script>

<header>
  <h1>Alpaca Generator 🦙</h1>
</header>
<main>
  <div class="alpaca">
    <h2>This is your alpaca!</h2>
    <AlpacaImg {alpaca} />
    <button on:click={randomize_alpaca}>Random! 🎲</button>
  </div>
  <div class="buttons">
    <div class="style-classes-buttons">
      <h2>Customize your Alpaca! ✨</h2>
      <div>
        {#each Object.keys(styles) as element}
          <button
            on:click={() => {
              selected_style = element;
            }}>{element}</button
          >
        {/each}
      </div>
    </div>
    <div class="style-buttons">
      {#if selected_style != ''}
        <h2>Style</h2>
        <div>
          {#each styles[selected_style] as style}
            <button
              on:click={() => {
                alpaca[selected_style] = style;
              }}
            >
              {style}
            </button>
          {/each}
        </div>
      {/if}
    </div>
  </div>
</main>
<footer>
  <p>
    Made by <a href="https://drawbu.me">drawbu</a> using Svelte to complete the
    <br /> «
    <a
      href="https://www.codementor.io/projects/web/alpaca-image-generator-website-ce2oc0eus8"
    >
      Alpaca image generator website
    </a>
    » challenge from
    <a href="https://www.codementor.io/projects">DevProjects</a>.
  </p>
</footer>

<style lang="scss">
  header {
    max-width: 80%;
    margin: auto;
    margin-top: 16px;
    margin-bottom: 32px;

    h1 {
      line-height: normal;
      text-decoration: underline #646cff 3px;

      @media (prefers-color-scheme: light) {
        text-decoration-color: #747bff;
      }
    }
  }
  main {
    margin: 20px auto;
    max-width: 400px;
    display: flex;
    flex-direction: column;
    gap: 64px;

    @media (min-width: 900px) {
      flex-direction: row;
      max-width: 900px;
    }

    .alpaca {
      h2 {
        margin-top: 16px;
        margin-bottom: 16px;
      }

      button {
        margin-top: 16px;
      }
    }

    .buttons {
      div {
        width: 400px;

        h2 {
          margin-top: 40px;
          margin-bottom: 8px;
          text-transform: uppercase;
          font-size: larger;
          text-align: left;
        }

        div {
          display: grid;
          grid-template-columns: repeat(3, 1fr);

          button {
            margin: 4px;
            text-transform: capitalize;
          }
        }
      }
    }
  }
  footer {
    max-width: 80%;
    margin: auto;
    margin-top: 32px;
    margin-bottom: 16px;
    opacity: 75%;
    transition: opacity 0.25s;

    &:hover {
      opacity: 100%;
    }
  }
</style>
