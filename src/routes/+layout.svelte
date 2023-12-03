<script lang="ts">
  import Header from './header.svelte';

  import '../app.css';
  import 'sanitize.css';
</script>

<div class="layout">
  <Header />

  <main>
    <slot />
  </main>
</div>
