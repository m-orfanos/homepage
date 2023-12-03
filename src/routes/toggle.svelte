<script lang="ts">
  import { fly } from 'svelte/transition';
  import { writable } from 'svelte/store';
  import { browser } from '$app/environment';

  import Sun from 'svelte-bootstrap-icons/lib/Sun.svelte';
  import Moon from 'svelte-bootstrap-icons/lib/Moon.svelte';

  let currentTheme = (browser && localStorage.getItem('color-scheme')) || 'dark';
  const theme = writable(currentTheme);

  function toggleTheme() {
    theme.update((currentTheme) => {
      const newTheme = currentTheme === 'dark' ? 'light' : 'dark';

      document.documentElement.setAttribute('color-scheme', newTheme);
      localStorage.setItem('color-scheme', newTheme);

      return newTheme;
    });
  }
</script>

<button on:click={toggleTheme} aria-label="Toggle theme">
  {#if $theme === 'dark'}
    <div in:fly={{ y: 10 }}>
      <Moon width="24" height="24" />
    </div>
  {:else}
    <div in:fly={{ y: -10 }}>
      <Sun width="24" height="24" />
    </div>
  {/if}
</button>

<style>
  button {
    padding: 0;
    font-weight: inherit;
    background: none;
    border: none;
    box-shadow: none;
    overflow: hidden;
  }

  button > * {
    display: flex;
    gap: var(--gap);
  }
</style>
