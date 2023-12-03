<script>
  import Github from 'svelte-bootstrap-icons/lib/Github.svelte';
  import Linkedin from 'svelte-bootstrap-icons/lib/Linkedin.svelte';
  import Twitter from 'svelte-bootstrap-icons/lib/TwitterX.svelte';

  import Toggle from './toggle.svelte';
</script>

<header class="header">
  <a class="header-info" href="/" title="Home">
    <h1 class="header-title">Miltiadis Orfanos</h1>
    <div class="header-tagline">Software Developer</div>
  </a>

  <nav class="header-nav">
    <a href="https://github.com/m-orfanos" title="Github">
      <Github width="24" height="24" />
    </a>
    <a href="https://www.linkedin.com/in/morfanos" title="Linkedin">
      <Linkedin width="24" height="24" />
    </a>
    <a href="https://twitter.com/morf4nos" title="Twitter">
      <Twitter width="24" height="24" />
    </a>
    <Toggle />
  </nav>
</header>

<style lang="scss">
  .header {
    align-items: center;
    background: var(--mantle);
    display: grid;
    grid-template-areas: 'logo nav';
    grid-template-columns: 1fr 1fr;
    justify-content: space-between;
    padding: var(--gap);

    a {
      text-decoration: none;
      &:hover {
        text-decoration: underline;
      }
      &:visited {
        color: inherit;
      }
    }

    .header-info {
      .header-title {
        font-size: 1.2em;
        margin: 0.15em 0;
      }
      .header-tagline {
        font-size: 0.8em;
      }
    }

    .header-nav {
      display: flex;
      gap: 0.8em;
      justify-content: end;
      margin: auto var(--gap);
      a {
        &:hover {
          color: var(--blue);
        }
      }
    }
  }
</style>
