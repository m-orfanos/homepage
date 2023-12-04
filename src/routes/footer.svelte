<footer>
  <div>
    <p>
      &copy {new Date().getFullYear()}. Built using <a href="https://kit.svelte.dev/">Sveltekit</a>
      and theme based on <a href="https://github.com/catppuccin/catppuccin">Catppuccin</a>.
    </p>
  </div>
</footer>

<style lang="scss">
  footer {
    border-top: 1px solid var(--rosewater);
    color: var(--lavender);
    font-size: var(--font-size-sm);
    line-height: var(--line-height-sm);

    div {
      display: flex;
      align-content: center;
      justify-content: center;
    }
  }
</style>
